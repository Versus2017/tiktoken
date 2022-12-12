# ⏳ tiktoken

tiktoken is a fast tokeniser.

```python
import tiktoken
enc = tiktoken.get_encoding("gpt2")
print(enc.encode("hello world"))
```

The open source version of `tiktoken` can be installed from PyPI:
```
pip install tiktoken
```

The tokeniser API is documented in `tiktoken/core.py`.


## Performance

`tiktoken` is between 3-6x faster than huggingface's tokeniser:

![image](./perf.svg)

Performance measured on 1GB of text using the GPT-2 tokeniser, using `GPT2TokenizerFast` from
`tokenizers==0.13.2` and `transformers==4.24.0`.

