# ⚡ Batch vs Stochastic Gradient Descent

## 📌 Project Overview

This project demonstrates and compares two fundamental optimization techniques used in Machine Learning and Deep Learning:

* **Batch Gradient Descent (BGD)**
* **Stochastic Gradient Descent (SGD)**

Using the **Social Network Ads** dataset, the notebook explores how different gradient descent strategies update model parameters and minimize the loss function.

The main focus is to understand the practical difference between **stable but computationally expensive updates** and **faster but noisier updates**.

---

## 🎯 Objective

The objectives of this project are to:

* Understand how Gradient Descent works
* Implement Batch Gradient Descent
* Implement Stochastic Gradient Descent
* Compare their weight-update behavior
* Analyze loss convergence
* Understand the trade-off between stability and speed
* Build a strong foundation for optimization in Deep Learning

---

## 📊 Dataset

The project uses the **Social Network Ads** dataset.

The dataset contains information about users and whether they purchased a product after seeing a social network advertisement.

### Important Features

* Age
* Estimated Salary

### Target Variable

* Purchased

The problem is treated as a **binary classification** task.

---

## 🧠 What is Gradient Descent?

Gradient Descent is an optimization algorithm used to minimize a model's loss function.

The basic idea is:

```text
Calculate Loss
     ↓
Calculate Gradient
     ↓
Update Weights
     ↓
Reduce Loss
     ↓
Repeat
```

The difference between Batch and Stochastic Gradient Descent is mainly **how much training data is used for each parameter update**.

---

## 🔵 Batch Gradient Descent

Batch Gradient Descent calculates the gradient using the **entire training dataset** before updating the model parameters.

### Characteristics

* Uses all training samples for each update
* Produces stable updates
* Convergence is generally smoother
* Can be computationally expensive for large datasets
* Requires more memory

```text
Entire Dataset
      ↓
Calculate Gradient
      ↓
Update Weights
```

---

## 🟠 Stochastic Gradient Descent

Stochastic Gradient Descent updates the model parameters using **one training example at a time**.

### Characteristics

* Uses one sample per update
* Updates happen frequently
* Can converge faster in some situations
* Training can be noisy
* Loss may fluctuate during optimization
* Works well with large datasets

```text
One Sample
    ↓
Calculate Gradient
    ↓
Update Weights
    ↓
Next Sample
```

---

## 🔬 Experiment Workflow

The notebook follows these steps:

1. Load the dataset
2. Explore the data
3. Select relevant features
4. Prepare input and target variables
5. Split the dataset into training and testing sets
6. Apply feature scaling where required
7. Implement Batch Gradient Descent
8. Implement Stochastic Gradient Descent
9. Train the models
10. Track the loss during training
11. Compare convergence behavior
12. Analyze the final results

---

## 📈 Batch GD vs SGD

| Feature          | Batch Gradient Descent | Stochastic Gradient Descent |
| ---------------- | ---------------------- | --------------------------- |
| Data per update  | Entire dataset         | One sample                  |
| Updates          | Less frequent          | Very frequent               |
| Convergence      | Smooth and stable      | Noisy                       |
| Memory usage     | Higher                 | Lower                       |
| Speed per update | Slower                 | Faster                      |
| Large datasets   | Can be expensive       | More suitable               |
| Loss curve       | Usually smoother       | Usually fluctuates          |

---

## 🔑 Key Learnings

### Batch Gradient Descent

BGD provides more stable gradient estimates because it considers the entire dataset before updating the parameters.

### Stochastic Gradient Descent

SGD introduces randomness into the optimization process because each update is based on a single sample.

This can make the loss curve noisy but can also help the model move quickly through the optimization process.

---

## ⚖️ The Main Trade-Off

The important difference can be summarized as:

```text
Batch GD
Stable + Smooth
      vs
SGD
Fast Updates + Noisy
```

Neither method is universally better.

The appropriate optimization strategy depends on:

* Dataset size
* Computational resources
* Model complexity
* Training time
* Convergence requirements

---

## 🛠️ Technologies Used

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Scikit-learn**
* **Jupyter Notebook**

---

## 📚 Concepts Demonstrated

* Gradient Descent
* Batch Gradient Descent
* Stochastic Gradient Descent
* Optimization
* Loss Minimization
* Weight Updates
* Model Convergence
* Binary Classification
* Feature Scaling
* Learning Rate
* Training Stability

---

## 🎓 Learning Outcomes

After completing this project, I developed a better understanding of:

* How gradient-based optimization works
* How weights are updated during training
* Why Batch GD produces smoother optimization
* Why SGD produces noisier updates
* How learning rate affects convergence
* The relationship between optimization and model training
* Why optimization techniques are fundamental to Deep Learning

---

## 🚀 Future Improvements

Possible extensions include:

* Implement **Mini-Batch Gradient Descent**
* Compare different learning rates
* Visualize weight updates
* Compare convergence speed
* Experiment with different batch sizes
* Compare GD, SGD, and Mini-Batch GD
* Apply the techniques to a larger dataset
* Compare custom implementations with Scikit-learn's optimization methods

---

## 💡 Final Takeaway

Batch Gradient Descent and Stochastic Gradient Descent are two fundamental approaches to optimization.

**Batch GD** provides stable and smooth updates by considering the entire dataset, while **SGD** performs frequent updates using individual samples and introduces more randomness.

Understanding these differences provides an important foundation for learning more advanced optimization techniques such as **Mini-Batch Gradient Descent, Momentum, RMSProp, and Adam**, which are widely used in modern Deep Learning.
