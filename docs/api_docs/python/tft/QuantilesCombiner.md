<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tft.QuantilesCombiner" />
<meta itemprop="path" content="Stable" />
<meta itemprop="property" content="__init__"/>
<meta itemprop="property" content="add_input"/>
<meta itemprop="property" content="create_accumulator"/>
<meta itemprop="property" content="extract_output"/>
<meta itemprop="property" content="initialize_local_state"/>
<meta itemprop="property" content="merge_accumulators"/>
<meta itemprop="property" content="num_outputs"/>
</div>

# tft.QuantilesCombiner

## Class `QuantilesCombiner`



Computes quantiles on the PCollection.

This implementation is based on go/squawd.
For additional details on the algorithm, such as streaming and summary,
see also http://web.cs.ucla.edu/~weiwang/paper/SSDBM07_2.pdf

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    num_quantiles,
    epsilon,
    bucket_numpy_dtype,
    always_return_num_quantiles=False,
    has_weights=False
)
```





## Methods

<h3 id="add_input"><code>add_input</code></h3>

``` python
add_input(
    summary,
    next_input
)
```



<h3 id="create_accumulator"><code>create_accumulator</code></h3>

``` python
create_accumulator()
```



<h3 id="extract_output"><code>extract_output</code></h3>

``` python
extract_output(summary)
```



<h3 id="initialize_local_state"><code>initialize_local_state</code></h3>

``` python
initialize_local_state(tf_config=None)
```

Called by the CombineFnWrapper's __init__ method.

This can be used to set non-pickleable local state.  It is used in
conjunction with overriding __reduce__ so this state is not pickled.  This
method must be called prior to any other method.

#### Args:

* <b>`tf_config`</b>: (optional) A tf.ConfigProto

<h3 id="merge_accumulators"><code>merge_accumulators</code></h3>

``` python
merge_accumulators(summaries)
```



<h3 id="num_outputs"><code>num_outputs</code></h3>

``` python
num_outputs()
```

Return the number of outputs that are produced by extract_output.

Returns: The number of outputs extract_output will produce.



