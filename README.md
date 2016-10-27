[![](https://jitpack.io/v/nomisRev/mockito-kotlin.svg)](https://jitpack.io/#nomisRev/mockito-kotlin)


# Forked from [https://github.com/nhaarman/mockito-kotlin](https://github.com/nhaarman/mockito-kotlin). Ported to Mockito 1 to support PowerMock!

# Mockito1-Kotlin 

A small library that provides helper functions to work with [Mockito](https://github.com/mockito/mockito) in Kotlin.

## Example

A test using Mockito1-Kotlin typically looks like the following:

```kotlin
@Test
fun a(){ 
  /* Given */
  val mock = mock<MyClass> {
    on { getText() } doReturn "text"
  }
  val classUnderTest = ClassUnderTest(mock)
  
  /* When */
  classUnderTest.doAction()
  
  /* Then */
  verify(mock).doSomething(any())
}
```
