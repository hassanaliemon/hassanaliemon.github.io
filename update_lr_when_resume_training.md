Recently, while training a model it stopped as there was no space left on disk to save 
the weights. Therefore, we resume the training using the weights. But here comes the twist! 
Upon resuming the training, the loss became scattered and inferencing those later models
were far away from expected result! Moreover, those later models were also far away 
from previous models. Then we started to dig down.

Upon digging down, we got the point where it caused problem and it was none other then 
learning rate. As we were resuming training from later epochs but the learning rate was the same.
As learning rate has a great impact on adjusting weights thus initilizing learning rate 
bigger caused the performance fall down!

I got it very easy in pytorch that it saves optimizer parameters differently and while 
loading those parameters we can change the learning rate

```py
checkpoint = torch.load(checkpoint_file)
model.load_state_dict(checkpoint['state_dict'])
optimizer.load_state_dict(checkpoint['optimizer_dict'])
# change learning rate for stable training
for param in optimizer.param_groups:
    param['lr'] = lr
```
[see here](https://stackoverflow.com/questions/51756913/in-pytorch-how-do-you-use-add-param-group-with-a-optimizer) further.

Also tensorflow we can do this like [below.](https://stackoverflow.com/questions/47994638/keras-resume-training-with-different-learning-rate)
