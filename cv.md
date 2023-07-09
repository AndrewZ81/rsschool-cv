## Profile:
Andrew Zaiko, Junior Python Developer
## My contacts:
* Mobile Phone: +375291059640
* Email: andrewzaiko@gmail.com
* GitHub: [AndrewZ81](https://github.com/AndrewZ81)
* Discord: andrew_z81
## About myself:
I work as an engineer and system administrator in a small trade company.
I'm responsible, accurate and purposeful.
## My skills and instruments:
* Algorithms and data structures
* Python v3
* Django
* Flask
* CI/CD
* Git
* PyCharm
## Code example:
```
def convert_from_csv_to_json(csv_file_name: str, json_file_name: str) -> Optional[str]:
    raw_data: Dict[int, Dict[str, Union[int, str]]] = {}
    try:
        file: IO = open(csv_file_name, encoding="utf-8")
    except FileNotFoundError:
        return f"Файл {csv_file_name} не найден"
    else:
        csv_file_data = csv.DictReader(file)
        for row in csv_file_data:
            try:
                key = row["id"]
            except KeyError:
                return "Ключ id не найден"
            else:
                raw_data[key] = row
    finally:
        file.close()

    with open(json_file_name, "w", encoding="utf-8") as file:
        json_data: str = json.dumps(raw_data, indent=4, ensure_ascii=False)
        file.write(json_data)

    return None
```
## Work experience:
One year course as a Python Developer: [SkyPro](https://sky.pro/)
## Education:
P.O.Sukhoi State Technical University of Gomel
## Languages:
* Russian: native
* English: B1
