# HowToNotes
General Collection of my How-To Notes


Convert R markdown to Jupyter/IPython notebook

```
        jupytext --to notebook kNearestNeighbors.Rmd
```

### Fasta file format
Split Fasta sequence by triplets

```
cat ${fasta} | grep -v ">" | fold -w3 | tr "\n" " "

```

Extract sequences matching a pattern in the Fasta header:

```
awk '/^>/ { ok=index($0,"XR_")!=0;} {if(ok) print;}' RefSeq221_homo_sapiens_protein_sequences.faa > RefSeq221_hs_XR_sequences.faa

```