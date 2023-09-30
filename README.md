# Philip-pizza_restaurant


# Restaurant-Pizza Flask Application

This is a simple Flask application that models restaurants, pizzas, and their relationships using SQLAlchemy as the Object-Relational Mapping (ORM) tool. It provides a basic structure for managing restaurant and pizza data, complete with data validation and serialization.

## Prerequisites

Before running this application, make sure you have the following prerequisites installed:

- Python (3.x recommended)
- Flask
- Flask-SQLAlchemy
- SQLAlchemy-Serializer

You can install these dependencies using `pip`:

```bash
pip install Flask Flask-SQLAlchemy sqlalchemy-serializer
```

## Getting Started

1. Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/restaurant-pizza-flask-app.git
```

2. Change into the project directory:

```bash
cd restaurant-pizza-flask-app
```

3. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

4. Install the required packages:

```bash
pip install -r requirements.txt
```

5. Run the Flask application:

```bash
flask run
```

The application will be available at [http://localhost:5000](http://localhost:5000).

## Project Structure

The project is structured as follows:

- `app.py`: The main Flask application file.
- `models.py`: Defines the SQLAlchemy models for `Restaurant`, `Pizza`, and `RestaurantPizza`.
- `templates/`: Contains HTML templates for rendering web pages.
- `static/`: Contains static files like CSS and JavaScript.
- `README.md`: This file.

## Usage

- Access the application in your web browser at [http://localhost:5000](http://localhost:5000).

- You can view and manage restaurants and pizzas through the web interface.

- The application also supports serialization and data validation for the `Restaurant` and `RestaurantPizza` models.

## Serialization

- The `SQLAlchemy-Serializer` library is used for serialization. It allows you to customize serialization rules for each model using the `serialize_rules` attribute.

- For example, in the `Restaurant` model, the `serialize_rules` attribute specifies that when serializing a `Restaurant` object, you should exclude the `pizzas.restaurant` and `-restaurant.pizza` attributes. Similar rules apply to other models.

## Data Validation

- Data validation is implemented using SQLAlchemy's `@validates` decorator. For instance, in the `Restaurant` model, the `validate_name` method checks that the name is less than 50 characters long, and in the `RestaurantPizza` model, the `validate_price` method ensures that the price falls between 1 and 30.

## Contributions

Contributions to this project are welcome. Feel free to fork the repository and submit pull requests for enhancements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
## Author
it is written by Philip Ogaye.
