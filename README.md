## B-REASO: A Multi-Level Multi-Faceted Bengali Evaluation Suite for Foundation Models

This is the repository for [B-REASO: A Multi-Level Multi-Faceted Bengali Evaluation Suite for Foundation Models](https://aclanthology.org/2025.findings-emnlp.492/) by [Md Tanzib Hosain](https://scholar.google.com/citations?user=3YexY9gAAAAJ&view_op=list_works&sortby=pubdate) and [Md Kishor Morol](https://scholar.google.com/citations?user=pjn3jg4AAAAJ) (Findings of EMNLP 2025).

<p align="center">
   🤗 <a href="https://huggingface.co/datasets/krarit/b-reaso" target="_blank">Hugging Face</a> 📃 <a href="https://aclanthology.org/2025.findings-emnlp.492/" target="_blank">Paper</a> 
</p>

## Evaluation

Clone the project, run:

	git clone https://github.com/kraritt/b-reaso && cd b-reaso

Prepare a new conda or python virtual environment, run:
	
 	pip install -r requirements.txt

Parse the model generation to extract the prediction.

Set environment variable ```API_KEY```.

```
$python3 b-reaso.py \
	--backend openai \
	--model [Model name] \
	--temperature [temperature for generation] \
	--max_tokens [max new tokens to generate] \
	--subsets [Choose subsets of B-REASO (names splited by comma) for evalutaion. Default is 'ALL'] \
	--log_dir [Directory for saving evaluation log] \
	--few_shot_num [The number for few shot example. Range: [0, 5]. Default is 5.] \
	--cot [Use CoT evaluation.]
```

## Reference

Please cite the paper if you use the dataset.

```
@inproceedings{hosain2025b,
  title={B-REASO: A Multi-Level Multi-Faceted Bengali Evaluation Suite for Foundation Models},
  author={Hosain, Md Tanzib and Morol, Md Kishor},
  booktitle={Findings of the Association for Computational Linguistics: EMNLP 2025},
  pages={9260--9274},
  year={2025}
}
```
