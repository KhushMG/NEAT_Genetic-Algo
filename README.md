# NEAT Genetic Algorithm
Steps: <br/>
1. Initialize a population <br/>
2. Evaluate individuals (fitness) <br/>
3. Select the best N individuals <br/>
4. Produce next generation via crossover and mutations <br/>
5. Algorithm repeats Steps 2-4 until desired fitness is reached or it can't find any more improvements <br/>

## Terminology: 

Genotypes: The actual genes, such as having the genes with traits for both green and blue eyes. <br/>
<br/>
Phenotypes: The visible traits. <br/>

**Why** are these relevant? <br/>
--> Even if someone has green eyes, they can produce offspring with blue eyes. It could happen that green eyes is the dominant trait in that certain person's case. <br/>

**How** does this relate to NEAT? <br/>
In the NEAT Genetic Algorithm, a neural network is a phenotype while the information for constructing the neural network is the genotype.

<br/>

Useful if we want to disable some traits in a neural network such as an edge but still want to be able to pass it to offspring. <br/>

## NEAT Algorithm's Genome
We want to encode genomes in a way that enables a useful crossover. <br/>

In other words, we want to take **two** neural networks that are performing well and <br/>
combine them in a way that typically preserves good properties

<br/>
We can do this by combine individual properties of corresponding neurons and synapses. <br/>

In the case when the two networks don't have the same structures, we can do the above <br/>
for the common parts. The excess/disjoint neurons from the more fit parent will be kept, <br/>
and the excess/disjoint neurons from the less fit parent will be discarded. <br/>

**How** do we even find the matching neurons and synapses? <br/>

The general idea is to assign a unique ID to each neuron. <br/>

Two given neurons are considered the same if their IDs match. <br/>

Now that neurons have IDs, we can use them to identify synapses. <br/>

Two synapses are the same if they connect the same neurons in the same direction. <br/>





