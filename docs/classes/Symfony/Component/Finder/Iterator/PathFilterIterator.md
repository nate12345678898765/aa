***

# PathFilterIterator

PathFilterIterator filters files by path patterns (e.g. some/special/dir).



* Full name: `\Symfony\Component\Finder\Iterator\PathFilterIterator`
* Parent class: [`\Symfony\Component\Finder\Iterator\MultiplePcreFilterIterator`](./MultiplePcreFilterIterator.md)




## Methods


### accept

Filters the iterator values.

```php
public accept(): bool
```











***

### toRegex

Converts strings to regexp.

```php
protected toRegex(string $str): string
```

PCRE patterns are left unchanged.

Default conversion:
    'lorem/ipsum/dolor' ==>  'lorem\/ipsum\/dolor/'

Use only / as directory separator (on Windows also).






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | Pattern: regexp or dirname |




***


## Inherited methods


### __construct



```php
public __construct(\Iterator $iterator, string[] $matchPatterns, string[] $noMatchPatterns): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iterator` | **\Iterator** | The Iterator to filter |
| `$matchPatterns` | **string[]** | An array of patterns that need to match |
| `$noMatchPatterns` | **string[]** | An array of patterns that need to not match |




***

### isAccepted

Checks whether the string is accepted by the regex filters.

```php
protected isAccepted(string $string): bool
```

If there is no regexps defined in the class, this method will accept the string.
Such case can be handled by child classes before calling the method if they want to
apply a different behavior.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |




***

### isRegex

Checks whether the string is a regex.

```php
protected isRegex(string $str): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




***

### toRegex

Converts string into regexp.

```php
protected toRegex(string $str): string
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |




***


***
