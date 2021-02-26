# PELT TESTING

Pelt is a library for testing your algorithms and generate 
various data type for these algorithm of differents ways.

## Usage

### Help

This function provides a summary of all the methods that Pelt has.

*Example:*

`
Pelt.help()
`

*Output:*


![Pelt Help](screenshots/help.PNG)


### Test

This function represent a unit test, it's the more basic functionality
in Pelt.

*Params: test( function, expected value, optional text)*

```
Pelt.test(10 + 5, 15)

Output: UNIT TEST [🕙 66275899.9337248]
        Success Test
        Expected Value: 15
        Ouput: 15 🥇

Pelt.test(sum( 20,20 ), 40)

Output: UNIT TEST [🕙 66275899.9337248]
        Success Test
        Expected Value: 40
        Ouput: 40 🥇

Pelt.test(sum( 25,10 ), 30)

Output: UNIT TEST [🕙 66275899.9337248]
        Success Test
        Expected Value: 30
        Ouput: 35 💥 
```

Per default, test() add a example text for your unit test, but also you can 
add a own text.

```
Pelt.test(mult( 2,10 ), 20,"Multiplication")

Output: MULTIPLICATION  [🕙 66275899.9337248]
        Success Test
        Expected Value: 20
        Ouput: 20 🥇
```


### Describe

This function represent a group of unit tests, it prints a detailed feedback of this tests group
Per default it add a example test, but also you can add a own text.

*Params: describe( matrix, optional text)*

```
Pelt.describe((
    ( sum(10,20),30 ),
    ( sum(20,20),40, "SUM OF NUMBERS" ),
    ( sum(25,25),55, "INCORRECT SUM OF NUMBERS" ),
),"SUMS")

Ouput: 🔍 SUMS 🔎

        UNIT TEST [🕙 61346599.9386544]

        Success Test 
        Expected Value: 30
        Ouput: 30 🥇
        ➖➖➖➖➖➖➖➖

        SUM OF NUMBERS [🕙 62347999.937653]

        Success Test
        Expected Value: 40
        Ouput: 40 🥇
        ➖➖➖➖➖➖➖➖

        INCORRECT SUM OF NUMBERS [🕙 63402799.936598]

        Failed Test
        Expected value: 55
        Ouput: 50 💥
        ➖➖➖➖➖➖➖➖
```

Without own text and with matrix:

```
Pelt.describe([
    [ sum(5,5),10 ],
    [ sum(13,12),25, "SUM OF NUMBERS" ]
])

Ouput: 🔍 TESTS GROUP 🔎

        UNIT TEST [🕙 81670499.918331]

        Success Test
        Expected Value: 10
        Ouput: 10 🥇
        ➖➖➖➖➖➖➖➖

        SUM OF NUMBERS [🕙 83254399.9167468]

        Success Test
        Expected Value: 25
        Ouput: 25 🥇
        ➖➖➖➖➖➖➖➖
```
