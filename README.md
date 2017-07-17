# Deploy ec2

## requirements
** python **
3.6.1

** pip **
```
pip install -r requirements.txt
```

## Create secret config file


### Project structure

```
project_folder/
    .config_secret/
        settings_common.json
        settings_debug.json
        settings_deploy.json
    django_app/
    ...
    ...
```

### settings_common.json example
```json
{
  "django": {
    "secret_key": "Django project secret key"
  }
}
```

### settings_debug & deploy .json example
```json
{
  "django": {
    "allowed_hosts": [
      "*"
    ]
  }
}
```

## runserver
```python
# local development
python3 manage.py runserver --settings=config.settings.debug
