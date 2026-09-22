# User Settings Manager

A command-line Python module for managing a dictionary of user configuration settings — add, update, delete, and view settings, with input validation and clear feedback messages for every action.

## Overview

This project implements a small settings-management system built entirely with core Python (dictionaries, tuples, string formatting, no external libraries). It was built as a self-taught practice project to reinforce data structure manipulation and function design.

## Features

- **Add a setting** : insert a new key-value pair, with a clear error if the key already exists
- **Update a setting** : change the value of an existing key, with a clear error if the key doesn't exist
- **Delete a setting** : remove a key-value pair, with a clear error if the key isn't found
- **View settings** : display all current settings in a readable, formatted list, or a message if none exist
- Keys and values are automatically normalized to lowercase for consistent storage and lookup
- Every action returns a descriptive success or error message

## Functions

| Function | Parameters | Description |
|---|---|---|
| `add_setting(settings, key_value)` | dict, tuple | Adds a new key-value pair if the key doesn't already exist |
| `update_setting(settings, key_value)` | dict, tuple | Updates an existing key's value |
| `delete_setting(settings, key)` | dict, str | Removes a key-value pair |
| `view_settings(settings)` | dict | Returns a formatted string of all current settings |

## Example

```python
test_settings = {
    "theme": "light",
    "notifications": "enabled",
    "volume": "medium",
}

print(add_setting(test_settings, ("Language", "English")))
# Setting 'language' added with value 'english' successfully!

print(update_setting(test_settings, ("theme", "Dark")))
# Setting 'theme' updated to 'dark' successfully!

print(view_settings(test_settings))
# Current User Settings:
# Theme: dark
# Notifications: enabled
# Volume: medium
# Language: english
```

## Running the project

```bash
python3 settings_manager.py
```

Running the file directly executes a small demo that exercises every function, including both success and error cases.

## What I practiced

- Working with dictionaries and tuples as function parameters
- Writing pure functions with predictable return values
- String formatting and case normalization
- Designing clear, consistent user-facing feedback messages

## Tech stack

- Python 3 (standard library only)
