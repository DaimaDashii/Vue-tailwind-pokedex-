# [Vue](https://vuejs.org/) && [Tailwind](https://tailwindcss.com) PokeDex Documentation

## Overview

Pokemon Gallery is a web application built using Vue.js and Tailwind CSS that displays a list of Pokemon and their details. The application fetches data from the PokeAPI.

## Structure

### HTML Structure

- Main container with id "app"
- Search input
- Grid for displaying Pokemon list
- Page navigation buttons
- Modal for displaying Pokemon details

### JavaScript Structure

The application uses [Vue 3](https://vuejs.org/) Composition API.

#### Main Components

1. `createApp`: Creates the Vue application instance
2. `setup()`: Main function that initializes state and methods

#### State Variables

- `pokemonList`: List of Pokemon currently displayed
- `allPokemon`: All Pokemon fetched from the API
- `isLoading`: Loading status
- `selectedPokemon`: Currently selected Pokemon for detailed view
- `searchQuery`: Search query string
- `currentEvolutionIndex`: Current evolution index
- `currentPage`: Current page number
- `itemsPerPage`: Number of items per page

#### Computed Properties

- `totalPages`: Calculates total number of pages
- `displayedPokemon`: Displays Pokemon based on search
- `canNavigatePrev` & `canNavigateNext`: Controls evolution navigation

##### Data Fetching

- `fetchAllPokemon()`: Fetches all Pokemon data from the API
- `showDetails(pokemon)`: Displays details of the selected Pokemon
- `showEvolutionDetails(index)`: Displays details of Pokemon evolution

##### Navigation

- `loadNext()` & `loadPrevious()`: Handles page navigation
- `navigateEvolution(direction)`: Navigates between Pokemon evolutions

##### Utility Functions

- `convertWeight(weight)`: Converts Pokemon weight to kg
- `convertHeight(height)`: Converts Pokemon height to cm

##### Search

- `searchPokemon()`: Performs Pokemon search

## Key Features

1. Displays a list of Pokemon with pagination
2. Allows searching for Pokemon by name
3. Shows detailed Pokemon information including stats, abilities, and evolution info
4. Enables navigation between Pokemon evolutions
5. Responsive design using Tailwind CSS

## API Integration

The application uses [Axios](https://axios-http.com/docs/intro) to make HTTP requests to the [PokeAPI](https://pokeapi.co/).

## Styling

Utilizes [Tailwind]CSS(https://tailwindcss.com) for styling, including grid layout and responsive design

## Usage

To use the application:

1. Load the page to see the list of Pokemon
2. Use the search bar to find specific Pokemon
3. Click on a Pokemon to view its details
4. In the details view, use the evolution navigation to explore different forms
5. Use the pagination buttons to navigate through the Pokemon list

## Performance Considerations

- The application implements caching for evolution data to reduce API calls
- Lazy loading is used for Pokemon images to improve initial load time

## Future Improvements

- Implement more advanced filtering options
- Add type-based color coding for Pokemon
- Integrate more detailed battle statistics
- Implement a compare feature for multiple Pokemon

This documentation provides an overview of the PokDex application, its structure, main features, and potential areas for future enhancement.
