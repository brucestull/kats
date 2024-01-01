# Command and links

## Commands

- `python manage.py makemigrations`
- `python manage.py migrate`
- `python manage.py createsuperuser --email FlynntKnapp@email.app --username FlynntKnapp`
- `python manage.py runserver`

- Create migrations for the `kitten_corner` app:
    - `python manage.py makemigrations kitten_corner`

- Create migrations for the `kat_food_corner` app:
    - `python manage.py makemigrations kat_food_corner`

## Install with Editing Enabled

- `pipenv install -e ..\kitten-corner\`
- `pipenv install -e ..\kat-food-corner\`
- `pipenv install -e ..\kat-corner\`

## Install from `tar.gz` Compressed Archive Files

- `pipenv install ..\kitten-corner\dist\KittenCorner-0.1.tar.gz`
- `pipenv install ..\kat-food-corner\dist\KatFoodCorner-0.1.tar.gz`
- `pipenv install ..\kat-corner\dist\KatCorner-0.1.tar.gz`

## Links

- [http://localhost:8000/](http://localhost:8000/)
- [http://localhost:8000/admin/](http://localhost:8000/admin/)

- [http://localhost:8000/kittens/](http://localhost:8000/kittens/)
- [http://localhost:8000/foods/](http://localhost:8000/foods/)
- [http://localhost:8000/kats/](http://localhost:8000/kats/)
