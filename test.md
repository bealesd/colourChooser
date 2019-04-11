<html>
<head>
</head>
<body>

    <h1>
    Variables and Scope
    </h1>
    
    <p>
    Like any language JavaScript has scopes and variables.
    </p>
    
    <p>
 Variables are pretty self explanatory, they store information. However what syntax you use to declare variables will make a massive difference to how your code behaves. Lets look at <em>'VAR'</em>
    </p>
    
    <h2>Var</h2>
    
    <p>Var is commonly is used to delcare a variables (commonly in older code bases, but sometimes in new ones). The function below declares a variable foo and assigns bar to it.</p>
    
    <p class='red'>
    <pre>function fooBar(){
    var foo = "bar"; //decalre a variable foo and assign bar to it
    console.log(foo); //print varibale foo to console
    }
    </br>fooBar(); //prints bar
    </pre>
    </p>
    <p>
    This behaviour seems completely reasonable, the variable foo is declared in the function fooBar. It exists only in the function scope of fooBar and cannot be accessed outside of that scope. So what is the issue with var?
    </p>
    
    <pre>
    for (var index = 0; index < 99 index++){
	    doSomeWork(index);
    }
    console.log(index); // index is 98
    </pre>
    
    <p>
    Thats odd, you would expect an error when calling index outside of the for loop. Well not with var, <em>it has no block scope</em>. The same would apply with a while, switch, if, etc.
    </p>
    <h4>
    Hoisting
    </h4>
    <p>
    So var has no block scope, but does it do anything else exciting. Well, yes! It support hosting.
    </p>
    <pre>
    function fooBar(){
	foo = "bar"; //assign bar to foo variable
	console.log(foo); //print foo
	var foo;
    }
    fooBar(); //prints bar
    </pre>
    <p>
I forgot to declare foo using var before I assigned a value to it. Guess what var doesn't care, as long as foo is decalred somewhere in the function, you can assign to it. If your wondering, thats called hoisting. So declarations are hostied, but what about declaration and assignment in one. Lets try it out.
    </p>

</body>
</html>
