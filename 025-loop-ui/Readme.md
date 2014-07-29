When you want to create some UI elements from a loop, it is tempting to use the dark power `eval(parse())`, e.g. `for (i in 1:10)` `eval(parse(text = paste0("uiOutput('id", i, "'"))))`, but this is almost always the wrong way to go in shiny. It makes the code obscure and insecure. This example shows you how to express the logic more naturally and securely without manually constructing the program code and evaluating it using the `eval(parse())` trick.