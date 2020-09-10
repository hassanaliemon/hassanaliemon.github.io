## Only for newbie:
	1. go to the competition page and click Rules
	2. click I understand and agree and do the procedure
	3. click data
	4. click I understand and agree
1) If you are in colab:
	!pip install --upgrade --force-reinstall --no-deps kaggle
   If in your local machine:
    !pip install kaggle
2) go to your account and scroll to API section and click Create New API Token
	It will download kaggle.json file to your local machine
3) from google.colab import files
  files.upload()
  and upload the kaggle.json file
4) ! cp kaggle.json ~/.kaggle/ #copy the json file 
5) ! chmod 600 ~/.kaggle/kaggle.json # change the permissions of the file.
6) Now go to the data section of the competition page and copy the download command. 
	For this page: https://www.kaggle.com/c/expedia-hotel-recommendations/ 
	it is:
	!kaggle competitions download -c expedia-hotel-recommendations

Now unzip the file using unzip command and enjoy your experiment!
