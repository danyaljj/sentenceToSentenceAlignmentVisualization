# Visualization of Sentence-to-sentence alignment
A sample visualization of sentence to sentence alignment with D3.js. Here is an screenshot: 

<img width="680" alt="screen shot 2016-07-27 at 4 17 56 pm" src="https://cloud.githubusercontent.com/assets/2441454/17195919/ac3136c2-5415-11e6-8ab0-576f99e9271b.png">

## How to use: 
Have a look inside `index.html`. The following variables are the only things you have to set: 
 - `text`: text in the first like 
 - `hyp`: text in the second line 
 - `textEntities`: list of entities in the first line 
 - `hypEntities`: list of entities in the second line 
 - `relations`: the connections between the entities 

To give more intuition, this is how these variables are set for the example shown in the screenshot: 

```javascript 
var text = "Ed O'Kelley was the man who shot the man who shot Jesse James.";
var hyp = "Ed O'Kelley was a good man.";

var textEntities = [
    // each line contains an id, and the span start and end 
    ['T1', [0, 11]],
    ['T2', [20, 23]],
    ['T3', [37, 40]],
];

var hypEntities = [
    ['H1', [0, 11]],
    ['H2', [18, 22]],
    ['H3', [23, 26]],
];

var relations = [
    // each line contains an id for relation, and id of the two entities being connected together 
    ['R1', 'T2', 'H1'],
    ['R2', 'T1', 'H2'],
    ['R3', 'T3', 'H3'],
];
```
