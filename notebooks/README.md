# notebooks

- `0_Template`
  - A general blueprint for running experiments. If you want to run a new experiment, copying this notebook is an easy starting point.
- `1_Sorting_Fixed_Length_Lists_with_One_Head`
  - Trained one-layer, one-head, attention-only transformer to sort lists of 5 non-repeating elements, with vocabulary of 64 tokens (+ 2 "special" `START` and `MID` tokens). First discovery of "ordering heads".
- `2_1L1H_attn_only,_with_repetition` 
  - Like `1` above but elements could repeat. This slightly altered behavior of ordering heads.
- `3_1L1H_attn_only,_long_list,_without_repetition`
  - Like `1` but with list length 50, instead of 5. Similar results.
- `4_Sorting_Fixed_Length_Lists_without_Heads_or_Repetition`
  - Zero-layer transformer (neither attention, nor MLP, mostly embedding + unembedding + positional encoding). Learned probabilistic bigrams, which it used to predict next token by incrementing the current one.
- `5_Sorting_Fixed_Length_Lists_without_Heads_but_with_Repetition`
  - Like `4` but with enabled repetition, which decreased performance and made those probabilistic bigrams assign significant probability to predicting a copy of the current token.
- `6_Ordering_Heads_in_Bigger_Models`
  - Testing whether ordering heads appear in bigger: with more attention heads and/or layers and/or with MLPs. There is some ordering head-like behavior in models with greater number of attention heads and/or layers, but it is much less consistent and something more complicated is going on. Adding MLP by itself does not seem to have an impact on development of the ordering head.
