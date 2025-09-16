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

**TL;DR:** If a hash has $m$ bits, you hit a ~50% collision chance after about $1.1774\\cdot 2^{m/2}$ random draws.  
That “square-root” law is why 160-bit SHA-1 fell and 256-bit hashes are still comfortable.
