# Loan Qualifier

Updating the lending software to prompt the user to save the qualifying loans as a new CSV file.

---

## Technologies

This project utilizes python 3.7.11 with the following libraries:

This project leverages python 3.7 with the following packages:

* [fire](https://github.com/google/python-fire) - For the command line interface, help page, and entry-point.

* [questionary](https://github.com/tmbo/questionary) - For interactive user prompts and dialogs.

* sys - which is inbuilt into python.

* pathlib - To interact with modules and to new csv file.

* csv library - To create a csv file.

---

## Installation Guide

Before running the application first install the following dependencies.

```python
  pip install fire
  pip install questionary
```

---

## Usage

To be able to prompt the user to save csv file, there needs to be data to be saved. If none then exit after msg.
If there is data, ask the user if they'll like to save and where.
If "Y" then save but if "N" don't do anything
``` if not qualifying_loans:
        sys.exit("Sorry, there are no qualifying loans!")

    saveFile = questionary.confirm("Would you like to save the qualifying loans?").ask()

    if saveFile:
        csvpath = questionary.text(
            "Please enter a filepath for the saved data: (qualifying_loans.csv)"
        ).ask()
        save_csv(Path(csvpath), qualifying_loans)
```

---

## Contributors

* Name: Chukwuma Ochu.
* Email: chukwuma.ochu@gmail.com

---

## License

gpl
