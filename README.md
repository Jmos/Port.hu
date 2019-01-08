# Port.hu

[![Latest Stable Version](https://poser.pugx.org/polakosz/porthu/v/stable)](https://packagist.org/packages/polakosz/porthu)
[![Total Downloads](https://poser.pugx.org/polakosz/porthu/downloads)](https://packagist.org/packages/polakosz/porthu)
[![License](https://poser.pugx.org/polakosz/porthu/license)](https://packagist.org/packages/polakosz/porthu)

[Port.hu](https://port.hu/) is one of the biggest hungarian movie database. This PHP library helps to search for movies and to get informations for a specific movie.

## Install

Via Composer

`$ composer require polakosz/porthu`

## Usage

```` php
use PoLaKoSz\PortHu\MoviePage;
...
$port = new MoviePage();

// returns a PoLaKoSz\PortHu\Models\PortMovie object
$movie = $port->get( 104833 );

var_dump( $movie );
````

```` php
use PoLaKoSz\PortHu\QuickSearch;
...
$search = new QuickSearch();

// returns an Array of PoLaKoSz\PortHu\Models\QuickSearchResult object
$movies = $search->get( 'Viskó' );

var_dump( $movies );
````

## Tests

### on Windows

Navigate to the root folder with the terminal and run one of the following code:

#### Integration Tests

`$ .\\vendor\\bin\\phpunit --bootstrap .\\vendor\\autoload.php --testdox .\\tests\\Integration`

or 

`$ .\\vendor\\bin\\phpunit --bootstrap .\\vendor\\autoload.php .\\tests\\Integration`
