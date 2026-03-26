# Same Network, Different Journey: How Learning Rate Changes Optimisation Dynamics in an ANN

This project investigates whether learning rate only affects how fast an artificial neural network (ANN) learns, or whether it fundamentally changes optimisation behaviour. The same ANN is trained on Fashion-MNIST with four learning rates (`0.0001`, `0.001`, `0.01`, `0.1`) to compare convergence speed, stability, final performance, and robustness across random seeds.

The tutorial focuses on optimisation dynamics rather than simple hyperparameter tuning. It shows that different learning rates create different training regimes: ineffective learning, slow progress, smooth convergence, or faster but less stable optimisation.

## Project Contents

- Jupyter notebook (`nagireddy_ml_code.ipynb`) containing the full experiment
- `outputs_lr/` — generated figures and summary results
- tutorial/report files — if included separately

## Dependencies

Install the required packages with:

```bash
pip install torch torchvision numpy matplotlib pandas                                                    How to Run

Open the Jupyter notebook and run all cells in order.

The notebook will:

download Fashion-MNIST if needed
train the same ANN with multiple learning rates
repeat each setting across multiple random seeds
generate figures for training loss, test accuracy, final metrics, and robustness
save outputs to the outputs_lr/ folder
Output Figures

The notebook generates:

figure_1_learning_rate_concept.png
figure_2_train_loss_curves.png
figure_3_test_accuracy_curves.png
figure_4_final_metrics.png
figure_5_seed_robustness.png

It also saves the final summary results to the output folder.

Main Question

The central question of the project is:

Does learning rate only control how fast an ANN learns, or does it fundamentally change how the optimisation process behaves?

Summary of Findings

The results show that learning rate changes more than training speed:

0.0001 is too small to support useful learning within the fixed epoch budget
0.001 learns slowly and is more sensitive across seeds
0.01 gives smooth and efficient convergence
0.1 achieves the strongest final performance, but follows a less smooth optimisation path
Reproducibility

The experiment uses a fixed ANN architecture, fixed training budget, and repeated random seeds so that differences can be attributed mainly to learning rate.

License

This project is released under the MIT License.
