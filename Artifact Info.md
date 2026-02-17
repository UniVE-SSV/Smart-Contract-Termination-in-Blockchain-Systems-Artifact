# Title
​
Smart Contract Termination in Blockchain Systems: Kill Switches, Emergency Stops, Pausing, and Halting Mechanisms (Artifact)

## Overview: What does the artifact comprise?

* Dockerfile: file to build the docker contaner
* artifact.tar: the archive containing the data for docker container

### Content of the Docker container

* what type of artifact
	* README file: instruction to reproduce raw paper results
	* scripts and file lists: scripts and data to automatize experimental evaluation
	* dataset: the dataset of files to analyze (Zellic 2023 Smart Contract Source Index)
	* results folder: reports generated after the script execution
* in which format
	* README file: .md
	* results:
		* Figures: .pdf (paper figures)
	* scripts and file lists:	
		* extract-sol-from-json: .py (to extract solidity files from json format on the dataset)
		* remove-sol-duplicates: .py (to remove duplicated solidity files on the dataset)
		* data-finder: .py (to reproduce paper results)
		* json-file-list: .txt (a pre-computed list of son file to analyze and extract solidity files)
		* sol-file-list: .txt (a pre-computed list of file to analyze without duplicates)
* can be found in which location
	* `/app/artifact/`

## Artifact Claims
​
* Which data or conclusions from the paper are generated/supported by the artifact components?
	* Reproduction of the raw results reported in the paper

* Which activities described in the paper have led to the creation of the artifact components?
	* Evaluation of existing Ethereum smart contracts

* What is the functionality/purpose of the artifact?
	* Reproduce the raw results of the paper
	* Provide a complete environment for analyzing the Ethereum smart contracts
​
## Getting Started

Build the docker container with the following command:

```
mkdir -p results
docker build --no-cache -t artifact-sc-termination .
docker run -it --name artifact-sc-termination -v $(pwd)/results:/app/artifact/results bash
```

Within the docker container:

* Open the file README.md located in `/app/artifact/` and follow the instructions.
​
