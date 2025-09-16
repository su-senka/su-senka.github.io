---
title: "The Birthday Problem & Hash Collisions"
layout: default
description: "How a classic probability puzzle predicts collisions in modern hash functions — with code."
tags: [probability, cryptography, hashing, monte-carlo]
date: 2025-09-16
---

<!-- MathJax (drop-in, no build tooling needed) -->
<script>
window.MathJax = { tex: { inlineMath: [['$', '$'], ['\\(', '\\)']] }, svg: {fontCache: 'global'} };
</script>
<script id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>

# The Birthday Problem & Hash Collisions

<em>How many random files before we should expect a collision?</em>

## From birthdays to hashes

For $k$ uniform draws from a space of size $n$, probability of no collision is

$$
P_0(k;n) = \prod_{i=0}^{k-1} \left(1 - \frac{i}{n}\right)
\approx \exp\!\left( -\frac{k(k-1)}{2n} \right).
$$
