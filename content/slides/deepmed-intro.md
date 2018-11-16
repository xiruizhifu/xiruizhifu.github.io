---
slides:
  theme: black
title: Deep Learning for Medicine and Healthcare
---

# Deep Learning for Medicine and Healthcare

[Deepmed Website](http://dm)

---

## What's `Deepmed`?

DeepMed is a deep learning framework for Medicine and Healthcare written in Python and it uses PyTorch as the backend engine 🚀.

---

## Why this Project?

The mission of this project is to make the power of state of the art deep learning models for medicine and healthcare available to anyone working in this area to build a better future of healthcare together.

---

**Use Deepmed if you need a Python library that:**

- Easy and fast try out state of the art models for medicine and healthcare;
- Support almost all kinds of neural networks because of the power provided by PyTorch;
- Runs seamlessly on both CPU and GPU.

---

## Package Structure

```
.
├── __init__.py
├── datasets
├── models
└── utils
```

---

### Subpackage: `datasets` 

```
datasets
├── __init__.py
├── common.py
├── cprd.py
├── metadata.py
└── ukb.py
```

---

### Subpackage: `models` 

```
models
├── __init__.py
├── losses.py
├── metrics.py
├── nn
│   ├── __init__.py
│   ├── attention.py
│   ├── autoencoder.py
│   ├── cnn.py
│   ├── layers.py
│   ├── module.py
│   └── rnn.py
├── optimizers.py
└── papers
    ├── __init__.py
    ├── deepcare.py
    ├── deeppatient.py
    ├── deepr.py
    ├── med2vec.py
    └── retain.py
```

---

### Subpackage: `utils` 

```
utils
├── __init__.py
├── decorators.py
├── device_utils.py
├── general_utils.py
├── model_utils.py
├── plotting_utils.py
├── preprocessing.py
└── training_utils.py
```

---

## Working with UK CPRD Dataset

- Easily check the basic information about the CPRD dataset;
- Retrive the patient data using very simple syntax;
- Many more useful functions to make your life easier.

[CPRD Example](http://dm/example/using-cprd-dataset.html)

---

## Working with UK Biobank Dataset

- Easily check the basic information about the UK Biobank dataset;
- Extract patient information and health outcomes in a straightforward way;
- Many more useful functions to make your life easier.

[UK Biobank Example](http://dm/example/using-ukb-dataset.html)

---

## Deep Learning Models

<div class="container">
<div class="col">
{{% fragment %}}

**Embeddings:**

- AutoEncoders
- RBM
- Word2Vec
- etc.

{{% /fragment %}}
</div>

<div class="col">
{{% fragment %}}

**Predictons:**

- RandomForest & XGBoost
- CNN & RNN
- Deep Forest
- etc.

{{% /fragment %}}
</div>

</div>

{{% fragment %}}
[`deepmed.models` Documentation](http://dm/modules.html#subpackage-models)
{{% /fragment %}}

---

# Questions?

[Ask me anything](https://yajiez.me)

[Online Documentation](http://dm)
