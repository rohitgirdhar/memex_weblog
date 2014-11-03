---
layout: post
title:  "CNN on Hussian Hotels dataset"
categories: CNN hotels
---

I tried CNN features for the hotels dataset as well.
Used `pool5` layer features, and `1 - cosine similarity` as the distance for retrieval/ranking.
Quantiative results are [here](http://pyrie.vmr.cs.cmu.edu/~rohit/projects/001_IR/002_CNN/results/cnn_matches/c001.html)

Quantitatively, performs slightly worse compared to ESVM.
{% highlight text %}
Without distractors
mP1 = 0.550000
mP3 = 0.418182
mP5 = 0.358182
mP10 = 0.284091
mP20 = 0.207727
at least 1 hit in 3 = 0.668182
at least 1 hit in 10 = 0.850000
{% endhighlight %}

For comparison, here is how ESVM performed (shared in an email sometime back)
{% highlight text %}
without distractors:
mP1 = 0.700000
mP3 = 0.562121
mP5 = 0.492727
mP10 = 0.386818
mP20 = 0.281591
at least 1 hit in top 3 = 0.786364
at least 1 hit in top 10 = 0.886364

with distractors:
mP1 = 0.672727
mP3 = 0.548485
mP5 = 0.468182
mP10 = 0.364545
mP20 = 0.265000
at least 1 hit in top 3 = 0.777273
at least 1 hit in top 10 = 0.850000
{% endhighlight %}


### Code Details
1. Evaluated using 
{% highlight matlab %}
>> esvm_compute_scores('/IUS/vmr105/rohytg/projects/001_ESVM/CNN/publish/www', '/IUS/vmr105/rohytg/projects/001_ESVM/CNN/publish/TestSet.txt')
{% endhighlight %}

