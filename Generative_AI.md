# Generative AI

## What is generative AI?
- Generative AI creates new content, such as text, images, audio, or code.
- It learns from examples and then generates data that is similar.
- Common models include GANs, VAEs, and large language models.

## Core concepts
- **Generator**: creates new samples.
- **Discriminator**: often used in GANs to distinguish real from generated samples.
- **Latent space**: a compressed representation used to generate new content.
- **Prompt**: input text or signal guiding generation.

## Example: Generating text with prompts

```python
from transformers import pipeline

generator = pipeline('text-generation', model='gpt2')
result = generator('The future of AI is', max_length=30, num_return_sequences=1)
print(result[0]['generated_text'])
```

This example uses a pretrained language model to continue a sentence.

## What to learn next
- How generative models are trained
- Differences between conditional and unconditional generation
- How to evaluate generated content
- Ethical considerations for generative AI
