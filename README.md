CommonSubstrings
================

####a method for finding all common strings for node.js
===
###Usage

####Quickstart
Give the array as input parameter.

    var tree = new SuffixTrie();
    tree.build(array);
    var fragmentResult1 = tree.weightByAverage();
    var fragmentResult2 = tree.weightByMax();

####Methods
There are two method to get the fragments:
- one is `weightByAverage()` : which rank the fragment by the product of the fragment length and fragment occurrence.
- one is `weightByMax()` : the process is trival, but main idea is rank the longest fragment in the longest string to the first.

Both method return an Object array, each element in the array include :  
  `source` : the index of the labels which contais this fragment,  
  `name` : the name of the fragment,  
  `weight` : the product of the fragment length and the fragment occurrence  


####Conifguration  
You may set the options of the algorithm when initialization.

    var tree = new SuffixTrie({
        minLength : 5, minOccurrence : 3 , debug : false
    });

The first two are standards for fragment, the debug decide whether to show console message.
the default values are:
`minLength` : 3
`minOccurrence` : 2
`debug` : true


###Extenal Librarys

###License

The MIT License
