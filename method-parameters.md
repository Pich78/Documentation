# Number of parameters in method signature

It is a good practice to not use a big number of parameters in a method signature.

The reasons are:
1) A big number of parameters in a function call can lead to confusion in types in near paramters;
2) When passing related parameters, if you have to add or remove one parameter, you have to modify the signature.

As a rule of thumb a good practice is to **not pass more than 3 parameters**.

If there are a lot of related parameters, use a class to enclasulate them and pass that class as a parameter.

