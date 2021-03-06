# Mentoring

## Reasonable Solutions
```kotlin
object Hamming {
    fun compute(left: String, right: String): Int {
        require(left.length == right.length) { "left and right strands must be of equal length." }
        return left.zip(right).count { it.first != it.second }
    }
}
```

```kotlin
object Hamming {
    fun compute(leftStrand: String, rightStrand: String): Int {
        require(leftStrand.length == rightStrand.length) { "left and right strands must be of equal length." }
        return leftStrand.zip(rightStrand).count { (left, right) -> left != right }
    }
}
```

## Common suggestions
* Function `require()` can be used to check for difference between strand lengths.
* Function `zip()` can be used to zip the strands together and `count()` to count the number of deviated chars.
