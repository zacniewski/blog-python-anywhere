### Commands on Python Anywhere

```bash
~ $ pip3.9 install --user pythonanywhere
Looking in links: /usr/share/pip-wheels
...
Successfully built pythonanywhere
Successfully installed contextlib2-21.6.0 pythonanywhere-0.12.1 schema-0.7.5 shellingham-1.5.4 tabulate-0.9.0 typer-0.12.3

~ $ pa_autoconfigure_django.py --python=3.10 https://github.com/zacniewski/blog-python-anywhere.git
< Running API sanity checks >
...
pythonanywhere.exceptions.SanityException: 
Could not find your API token.
You may need to create it on the Accounts page?
You will also need to close this console and open a new one once you've done that.
```

After creating API Token in `Account -> API Token` section:  
```bash
~ $ pa_autoconfigure_django.py --python=3.10 https://github.com/zacniewski/blog-python-anywhere.git
< Running API sanity checks >
   \
    ~<:>>>>>>>>>
Cloning into '/home/zacniewski/zacniewski.pythonanywhere.com'...
remote: Enumerating objects: 43, done.
remote: Counting objects: 100% (43/43), done.
remote: Compressing objects: 100% (35/35), done.
remote: Total 43 (delta 3), reused 43 (delta 3), pack-reused 0
Unpacking objects: 100% (43/43), 9.07 KiB | 9.00 KiB/s, done.
< Creating virtualenv with Python3.10 >
   \
    ~<:>>>>>>>>>
    
...

 Pip installing -r                                                     |
| /home/zacniewski/zacniewski.pythonanywhere.com/requirements.txt (this |
| may take a couple of minutes)      

...

SystemCheckError: System check identified some issues:
ERRORS:
?: (staticfiles.E002) The STATICFILES_DIRS setting should not contain the STATIC_ROOT setting.
WARNINGS:
?: (staticfiles.W004) The directory '/home/artur/Desktop/PROJECTS/materials-about-internet-apps-and-www-websites/blog-185ic/static' in the STATICFILES_DIRS setting does not exist.
?: (staticfiles.W004) The directory '/home/zacniewski/zacniewski.pythonanywhere.com/static' in the STATICFILES_DIRS setting does not exist.


```