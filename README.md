#SwiftRandom
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](http://mit-license.org)
[![Language](https://img.shields.io/badge/language-swift-orange.svg)](https://developer.apple.com/swift)
[![Platform](https://img.shields.io/badge/platform-iOS%20%26%20OS%20X-lightgrey.svg
)](https://developer.apple.com/resources/)


SwiftRandom is collection of pseudorandom generators from various statistical distributions and functions for pseudorandom array sampling.

##Available psuedorandom generators:

* Discrete distributions:
	* Discrete uniform distribution
	* Binomial distribution
	* Geometric distribution
* Continuous distributions:
	* Continuous uniform distribution
	* Exponential distribution
	* Normal (Gaussian) distribution

##Sampling functions:

* Sampling with replacement
* Sampling without replacement
* Sampling with replacement with given probabilities		 	

##How to use it?

```swift
import SwiftRandom

//Single pseudorandom normal variable
//with mean 0 and standard deviation 1
let x = randNormal(0, 1)

//Array of pseudorandom independent normal variables 
//with mean 0 and standard deviation 1 and length 10
let sample = randNormals(0, 1, 10)

//Sampling from array:

//with replacement
let numbers = [10, 11, 45, 1, 0, 4]
let bootstrapSample = sampleWithReplacement(numbers, 10)

//without replacement
let names = ["John", "Bob", "Anna", "Alice", "Chris", "Luke"]
let usersOrder = sampleWithoutReplacement(names, 4)

//with given probabilities
let letters = ["a", "b", "c", "d", "e"]
let probabilities = [0.5, 0.05, 0.05, 0.1, 0.3] //probabilities have to sum to 1

let randomLetters = sampleWithProbs(letters, probabilities, 10)
```
