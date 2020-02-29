# laravel-string-similarities

Compare two string and get a similarity percentage.

## Install

You can install this package via composer:

``` bash
$ composer require ammarmidani/laravel-string-similarities
```

## Usage

``` php
$comparison = new \AmmarMidani\StringSimilarity\Compare();

// the functions returns similarity percentage between strings
$jaroWinkler = $comparison->jaroWinkler('first string', 'second string'); // JaroWinkler comparison
$levenshtein = $comparison->levenshtein('first string', 'second string'); // Levenshtein comparison
$smg = $comparison->smg('first string', 'second string'); // Smith Waterman Gotoh comparison
$similar = $comparison->similarText('first string', 'second string'); // Using "similar_text()"

// This next one will return an array containing the results of all working comparison methods
// plus an array of 'data' that includes the first and second string, and the time in second it took to run all
// comparison. BE AWARE that comparing long string can results in really long compute time!
$all = $comparison->all('first string', 'second string');
```