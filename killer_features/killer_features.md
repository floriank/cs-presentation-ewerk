!SLIDE center transition=fade

# Killer Features


!SLIDE center transition=fade

# Killer Feature #1
# ** Whitespace **

!SLIDE small transition=fade

    @@@ ruby
    if true
      console.log('hell yeah')
    else
      console.log('fuuuuu')

    kids =
      brother:
        name: "Max"
        age:  11
      sister:
        name: "Ida"
        age:  9

!SLIDE center transition=fade

# Killer Feature #2
# ** Operatoren **

!SLIDE small transition=fade

<table class="definitions">
  <tbody>
    <tr><th>CoffeeScript</th><th>JavaScript</th></tr>
    <tr><td><tt>is</tt></td><td><tt>===</tt></td></tr>
    <tr><td><tt>isnt</tt></td><td><tt>!==</tt></td></tr>
    <tr><td><tt>not</tt></td><td><tt>!</tt></td></tr>
    <tr><td><tt>and</tt></td><td><tt>&amp;&amp;</tt></td></tr>
    <tr><td><tt>or</tt></td><td><tt>||</tt></td></tr>
    <tr><td><tt>true, yes, on</tt></td><td><tt>true</tt></td></tr>
    <tr><td><tt>false, no, off</tt></td><td><tt>false</tt></td></tr>
    <tr><td><tt>@, this</tt></td><td><tt>this</tt></td></tr>
    <tr><td><tt>of</tt></td><td><tt>in</tt></td></tr>
    <tr><td><tt>in</tt></td><td><i><small>no JS equivalent</small></i></td></tr>
  </tbody>
</table>


!SLIDE center transition=fade

# Killer Feature #3
# ** Funktionssyntax **

!SLIDE small transition=fade

    @@@ ruby
    square = (x) -> x * x
    cube   = (x) -> square(x) * x

    fill = (container, liquid="coffee") ->
      "Filling the #{container} with #{liquid}..."

    fill "bottle"


!SLIDE center transition=fade

# Killer Feature #4
# ** Vererbung **

!SLIDE small transition=fade

    @@@ ruby
    class Animal
      constructor: (@name) ->

      move: (meters) ->
        console.log "#{@name} moved #{meters} m."

    class Snake extends Animal
      move: ->
        console.log "Slithering..."
        super 5

    class Horse extends Animal
      move: ->
        console.log "Galloping..."
        super 45

    sam = new Snake "Sammy the Python"
    tom = new Horse "Tommy the Palomino"

    sam.move()
    tom.move()



!SLIDE center transition=fade

# Killer Feature #5
# ** Scoping **

!SLIDE small transition=fade

    @@@ javascript
    // CoffeeScript
    outer = 1
    changeNumbers = ->
      inner = -1
      outer = 10
    inner = changeNumbers()


    // Javascript
    var changeNumbers, inner, outer;
    outer = 1;
    changeNumbers = function() {
      var inner;
      inner = -1;
      return outer = 10;
    };
    inner = changeNumbers();



!SLIDE center transition=fade

# Killer Feature #6
# ** Listen **

!SLIDE small transition=fade

    @@@ ruby
    eat food for food in ['toast', 'cheese', 'wine']

!SLIDE center transition=fade

# Killer Feature #7
# ** Array Operationen **

!SLIDE small transition=fade

    @@@ ruby
    numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

    copy = numbers[0...numbers.length]

    middle = copy[3..6]

    numbers[3..6] = [-3, -4, -5, -6]

!SLIDE center transition=fade

# Killer Feature #7
# ** "Everything is an Expression" **

!SLIDE small transition=fade

    @@@ ruby
    grade = (student) ->
      if student.excellentWork
        "A+"
      else if student.okayStuff
        if student.triedHard then "B" else "B-"
      else
        "C"

!SLIDE center transition=fade

# Killer Feature #8
# ** Splats **

!SLIDE small transition=fade

    @@@ ruby
    awardMedals = (first, second, others...) ->
      gold   = first
      silver = second
      rest   = others

    contenders = ["Michael Phelps" ,"Liu Xiang", "Yao Ming"]

    awardMedals contenders...

!SLIDE center transition=fade

# Killer Feature #8
# ** String Interpolation **

!SLIDE small transition=fade

    @@@ ruby
    sentence = "#{ 22 / 7 } is a decent approximation of Ï€"