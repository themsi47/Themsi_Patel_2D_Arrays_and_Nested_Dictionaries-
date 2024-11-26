# Themsi_Patel_2D_Arrays_and_Nested_Dictionaries
# Themsi Patel - 2D Arrays and Nested Dictionaries 
# 27 November, 2024
# Description: This program uses nested dictionaries to define characters, locations, and inventory,
# prints their descriptions, and completes exercises 6-7 to 6-11 from Python Crash Course.

# Characters and Traits
characters = {
    "Aragorn": {  # Character name as the key
        "class": "Ranger",  # Class of the character
        "weapon": "Sword",  # Weapon used by the character
        "strength": 18,  # Strength attribute of the character
    },
    "Gandalf": {
        "class": "Wizard",
        "weapon": "Staff",
        "strength": 20,
    },
    "Legolas": {
        "class": "Archer",
        "weapon": "Bow",
        "strength": 16,
    }
}

# Locations and Descriptions
locations = {
    "Rivendell": {  # Location name as the key
        "type": "Elven city",  # Type of the location
        "description": "A tranquil haven for travelers and elves.",  # Description of the location
    },
    "Moria": {
        "type": "Dwarven city",
        "description": "Dark tunnels full of secrets and danger.",
    },
    "Shire": {
        "type": "Hobbit village",
        "description": "Lush green lands with peaceful homes.",
    }
}

# Inventory and Characteristics
inventory = {
    "Sword of Flame": {  # Inventory item name as the key
        "damage": 50,  # Damage value of the item
        "weight": 15,  # Weight of the item
    },
    "Healing Potion": {
        "healing": 20,  # Healing value of the potion
        "weight": 1,  # Weight of the potion
    },
    "Bow of Precision": {
        "damage": 35,  # Damage value of the bow
        "weight": 8,  # Weight of the bow
    }
}

# Function to print details of a nested dictionary
def print_nested_dict_as_sentences(title, data):
    """Prints the details of a nested dictionary in a formatted manner.

    Args:
        title (str): The title for the section being printed.
        data (dict): The nested dictionary containing the data to print.
    """
    print(f"\n{title}:")  # Print the title of the section
    for name, attributes in data.items():  # Iterate through each item in the dictionary
        # Create a list of attribute descriptions
        attributes_list = [f"{attribute_name.replace('_', ' ').title()}: {attribute_value}" for attribute_name, attribute_value in attributes.items()]
        attributes_sentence = ", ".join(attributes_list)  # Join descriptions into a sentence
        print(f"{name} has the following attributes: {attributes_sentence}.")  # Print the attributes

# Print Characters
print_nested_dict_as_sentences("Characters", characters)

# Print Locations
print_nested_dict_as_sentences("Locations", locations)

# Print Inventory
print_nested_dict_as_sentences("Inventory", inventory)

# Python Crash Course Exercises 6-7 to 6-11

# 6-7. People
people = [
    {"name": "Alice", "age": 28, "job": "Engineer"},  # Person dictionary with name, age, and job
    {"name": "Bob", "age": 34, "job": "Doctor"},
    {"name": "Cathy", "age": 25, "job": "Artist"},
]

print("\nPeople:")  # Print header for people section
for person in people:  # Iterate through the list of people
    print(f"{person['name']} is {person['age']} years old and works as an {person['job']}.")  # Print person details

# 6-8. Pets
pets = [
    {"name": "Max", "type": "dog", "owner": "Alice"},  # Pet dictionary with name, type, and owner
    {"name": "Mittens", "type": "cat", "owner": "Bob"},
    {"name": "Tweety", "type": "bird", "owner": "Cathy"},
]

print("\nPets:")  # Print header for pets section
for pet in pets:  # Iterate through the list of pets
    print(f"{pet['name']} is a {pet['type']} owned by {pet['owner']}.")  # Print pet details

# 6-9. Favorite Places
favorite_places = {
    "Alice": ["Paris", "New York", "Tokyo"],  # List of favorite places for each person
    "Bob": ["Rome", "Venice"],
    "Cathy": ["Sydney"],
}

print("\nFavorite Places:")  # Print header for favorite places

# 6-10. Favorite Numbers
favorite_numbers = {
    "Alice": [7, 42],  # Alice's favorite numbers
    "Bob": [3, 8],     # Bob's favorite numbers
    "Cathy": [12, 15, 21],  # Cathy's favorite numbers
}

print("\nFavorite Numbers:")  # Print header for favorite numbers section
for person, numbers in favorite_numbers.items():  # Iterate through each person and their favorite numbers
    numbers_sentence = ', '.join(map(str, numbers))  # Convert numbers to strings and join them into a single sentence
    print(f"{person}'s favorite numbers are: {numbers_sentence}.")  # Print the person's name and their favorite numbers

# 6-11. Cities
cities = {
    "Paris": {  # City name as the key
        "country": "France",  # Country where the city is located
        "population": "2.1 million",  # Population of the city
        "fact": "Known as the city of light.",  # Interesting fact about the city
    },
    "Tokyo": {  # City name as the key
        "country": "Japan",  # Country where the city is located
        "population": "37 million",  # Population of the city
        "fact": "Largest city in the world by population.",  # Interesting fact about the city
    },
    "New York": {  # City name as the key
        "country": "USA",  # Country where the city is located
        "population": "8.4 million",  # Population of the city
        "fact": "Known as the Big Apple.",  # Interesting fact about the city
    },
}

print("\nCities:")  # Print header for cities section
for city, attributes in cities.items():  # Iterate through each city and its attributes
    # Print city details including country, population, and fact
    print(f"{city} is located in {attributes['country']} with a population of {attributes['population']}. It is {attributes['fact']}.")
    
    
