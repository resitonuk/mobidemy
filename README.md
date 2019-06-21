#Mobidemy#

Tüm hakları Avukat Reşit Onuk'a aittir. 
GPL3 Lisansı

##Proje ile gönderilmiş bulunan kurulum yönergesidir. 

Virtualenv folder was ignored. You can use these on the project folder:

$ virtualenv env

$ source ./env/bin/activate

$ pip install -r requirements.txt

##Database Information##

Name     : 'mobidemy_development'

User     : 'fordjango'

Password : '123456'

If you want latest dev db dump

$ sudo -u postgres psql mobidemy_development < temp/mobidemy-dev_db_dump.sql

OR for initial setup (run in virtual env)

$ python manage.py migrate_schemas --shared

$ python manage.py loaddata fixtures/initial_data.json # For initial data.

For tenant superuser(Tenant admin)

$ manage.py createsuperuser --username='admin' --schema=institution1

Take affect to all schemas for every changes

$ python manage.py migrate_schemas

$ python manage.py makemigrations

For institution schema only

$ python manage.py migrate_schemas --schema=institution1

#test#

### Good luck! ###
