#Install Genie Acs  
#bisa ikutin dokumentasi dari website genieacs ==> https://docs.genieacs.com/en/latest/installation-guide.html <==  
#atau gunakan script berikut  


> sudo apt install git curl -y  
> sudo git clone https://github.com/Dikimahendra/ACS-DB  
> sudo cd ACS-DB  
> sudo chmod +x install.sh  
> sudo bash install.sh  
  
#Tunggu proses instalasi..  
  
#Backup Db Lama / Db Default Genieacs  
  
> sudo mkdir backup-geniesacs  
> sudo mongodump --db genieacs --out backup-genieacs  
  
#Upload DB full parameter  
> sudo mongorestore --db=genieacs --drop db-genieacs-fullparam  

  
#user : admin  
#pass  : admin  
  
#======untuk mengembalikan acs seperti default silahkan ketik script berikut======#  

> sudo mongorestore --db=genieacs --drop backup-genieacs  
