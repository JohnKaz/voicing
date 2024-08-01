# euphonics

## Description
This function modifies all sentences in a CoNLL-U formatted file containing voicing annotation in their 10th (MISC) collumn.
More specifically, it duplicates this annotation and appends it as an extra feature of the token to its 6th (FEATS) collumn.

An example of a token containing such annotation is feature below

#### Original token:
```
5	ντως	εγώ	PRON	AdBa	Case=Gen|Number=Plur|Person=3|Poss=Yes|PronType=Prs	4	nmod	_	Voicing=Voiced
```

#### Modified token:
```
5	ντως	εγώ	PRON	AdBa	Case=Gen|Number=Plur|Person=3|Poss=Yes|PronType=Prs|Voicing=Voiced	4	nmod	_	Voicing=Voiced
```

## Usage
Simply run the "voicing" function on your desired input_file and output_file. 
Bear in mind that the altered sentences will be appended to the output_file so said file should be empty / not exist before function is run.

### Example
```
with open("input.conllu", "r") as file:
    voicing(file, "output.conllu") # output file is created when function is run
```
