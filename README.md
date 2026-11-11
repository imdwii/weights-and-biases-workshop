# Weights & Biases Automated Hyperparameter Optimization

A guided hyperparameter optimization workshop for **EGR 444: Advanced AI/ML for Engineering Applications** at the University of Rhode Island.

In this lesson, we use Weights & Biases (W&B) to perform automated hyperparameter optimization. We will go through the full workflow: inspecting the data, setting up W&B accounts, running a basic example, running an example with W&B Sweeps, and investigating differences in parameter importance.

## Project use cases and limitations


## Learning outcome

By the end of this workshop, you will be able to:
1. Parameterize a PyTorch model and training hyperparameters so that they can be dynamically read from wandb.config.
2. Configure and launch an automated W&B Sweeps using different methods such as bayes, random, and grid to systematically search for optimal hyperparameter combinations.
3. Analyze W&B sweep dashboards to select an optimal model checkpoint based on test loss and training stability rather than manual guesswork.

## Setup

### Run locally

Use **Python 3.12**. Save the project wherever you prefer on your machine, then open a terminal in that folder.

#### macOS or Linux

```bash
python3.12 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

#### Windows PowerShell

```powershell
py -3.12 -m venv .venv
.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

## Numbered tutorial

1. Go through the Setup section above
2. Open tutorial.ipynb
3. Click Select Kernel and if prompted install Python + Jupyter
4. Select kernel as Python Environments
5. Select your .venv folder
6. When trying to run the first code cell if prompted install the ipykernel package. Run the first code cell to download the data.
7. Create a W&B account using your URI email: https://wandb.ai/site/
8. After creating an account, click your profile
9. Click API keys
10. Click + New key
11. Name it wandb_workshop_key
12. Set expiration to 7 days
13. Click Create API key
14. Copy the key to your clipboard and save it somewhere secure. This will be used to sign into your account for one of the notebook cells.
15. Run the code cell with wandb.login(): 
    - Enter 2
    - Paste your API key and hit enter
16. Your account should now be connected to the notebook and you can now run the W&B related cells.

## Expected results

1. Model accuracy should achieve about 87%–90% test accuracy (test_acc) and a test loss below 0.35 (test_loss).
2. Populated W&B project dashboard comparing all trials and saved .pth model checkpoints in your outputs/ directory.

## Troubleshooting guidance

## Sources

- [PyTorch example code](https://docs.pytorch.org/tutorials/beginner/basics/quickstart_tutorial.html)
- [Weights and Biases documentation](https://docs.coreweave.com/forge-home)
- [Formatting & structure](https://github.com/mchiovaro/object-detection-lesson)
