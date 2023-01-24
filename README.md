# One Attention Head Is All You Need for Sorting Fixed-Length Lists

*This work was produced as a part of the [Mechanistic Interpretability Hackathon](https://itch.io/jam/mechint) organized by [Apart Research](https://apartresearch.com). We are grateful to Apart Research for organizing it and for helping with our project as well as to Neel Nanda whose [list of concrete open problems in mechanistic interpretability](https://www.lesswrong.com/posts/ejtFsvyhRkMofKAFy/200-cop-in-mi-interpreting-algorithmic-problems#Problems) inspired it.*

> We trained a single layer attention-only transformer to sort a fixed-length list of non-repeating tokens. It turned out to implement an operation consisting of looking into the unsorted list and searching for tokens that are greater than the current token, giving greater weight to the ones that are closer in the ordering. This attention pattern was clearest in transformers with one attention head, whereas increasing the number of heads led to development of more complex algorithms. We further explored how the same task was accomplished by zero-layer models as well as how varying list length, vocabulary size, and model complexity impacts the results.

The full report/paper is available [here](https://matthewbaggins.itch.io/one-attention-head-is-all-you-need-for-sorting-fixed-length-lists).

- `notebooks` - Jupyter notebooks used to train and test these models and explore their inner workings
- `models` - state dicts and training histories from notebooks 1-4
