# Requirements

## Data model

The SoupSON data format aims to represent the following meal preparation
entities and constraints:

- Recipe
  - A recipe contains one or more ingredients
  - A recipe produces one meal

- Ingredients
  - An ingredient must have an identifier
  - An ingredient must have an associated quantity
  - An ingredient may have an associated unit scale (e.g. 'grams')
  - An ingredient may be optional
  - An ingredient may list one or more substitute ingredients

- Equipment
  - An item of equpiment must have an identifier
  - An item of equipment may list one or more substitute items of equipment

- Temperature
  - A temperature must have an associated value
  - A temperature must have an associated unit scale (e.g. 'celsius')

- End condition
  - An end condition must have an associated ingredient
  - An end condition must have an associated expression
    - An expression must contain a sensory indicator (i.e. 'appearance')
    - An expression must contain a value (i.e. 'golden')
    - Sensory indicators include
      - appearance
      - sound
      - taste
      - smell
      - feel
      - temperature
      - duration
      - size

- Methods
  - A method must have an identifier
  - A method may reference one or more items of equipment
  - A method may specify a temperature
  - A method may specify an end condition

- Preparation steps
  - A step must have one or more inputs
  - A step may have one or more outputs
  - An input must be either an ingredient or a preparation step
  - An output must be either a preparation step or a meal
  - A step may reference one or more methods

- Meal
  - A meal must have a name
  - A meal may specify an integer number of servings
  - A meal may specify one or more serve-with suggestions (i.e. 'cooked rice')
