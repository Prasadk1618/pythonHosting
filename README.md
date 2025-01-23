# paython app hosting with amazon Linux

  ###  steps:-
	1. update package manager.
 ```bash
	 SUDO YUM UPDATE -Y
```
	2. check paython virson.
```bash	
  paython -v
```
	3. install paython & virsual envornment
	- sudo yum install paython3-venv paython3-pip -y
	4. create directory
	- mkdir dirname
	5. go the directory
	- cd dirname
	6. create virtual envornment
	- paython3 -m venv myenv
	7. active virtual envornment
	- source myenv/bin/activate
	8. create requirement.txt & add list of software
	- nano requirement.txt
	9. install the requirement.txt
	- pip install -r requirement.txt
	10. create app.py file & add the app code
	- nano app.py
	11. start the GUNICORN 
	- gunicorn --bind 0.0.0.0:8000 myapp:app
	12. start or run background GUNICORN 
	- gunicorn --workers 3 --bind 0.0.0.0:8000 myapp:app&
