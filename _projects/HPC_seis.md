---
layout: page
title: High Performance Computing on Cross-correlation Functions
description: Produced CUDA parallel programs to compute cross-correlation functions of large-scale seismic data on GPU
img: assets/img/publication_preview/seis_wave.gif
importance: 1
category: Others
report: ../assets/pdf/HPC.pdf
tag1: High Performance Computing
tag1_style: secondary
tag2: Seismology
tag2_style: warning
---

<div class="report text-right">
    <a href="../../assets/pdf/HPC.pdf">
    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="currentColor" class="bi bi-file-earmark-pdf-fill" viewBox="0 0 16 16">
        <path d="M5.523 12.424c.14-.082.293-.162.459-.238a7.878 7.878 0 0 1-.45.606c-.28.337-.498.516-.635.572a.266.266 0 0 1-.035.012.282.282 0 0 1-.026-.044c-.056-.11-.054-.216.04-.36.106-.165.319-.354.647-.548zm2.455-1.647c-.119.025-.237.05-.356.078a21.148 21.148 0 0 0 .5-1.05 12.045 12.045 0 0 0 .51.858c-.217.032-.436.07-.654.114zm2.525.939a3.881 3.881 0 0 1-.435-.41c.228.005.434.022.612.054.317.057.466.147.518.209a.095.095 0 0 1 .026.064.436.436 0 0 1-.06.2.307.307 0 0 1-.094.124.107.107 0 0 1-.069.015c-.09-.003-.258-.066-.498-.256zM8.278 6.97c-.04.244-.108.524-.2.829a4.86 4.86 0 0 1-.089-.346c-.076-.353-.087-.63-.046-.822.038-.177.11-.248.196-.283a.517.517 0 0 1 .145-.04c.013.03.028.092.032.198.005.122-.007.277-.038.465z"/>
        <path fill-rule="evenodd" d="M4 0h5.293A1 1 0 0 1 10 .293L13.707 4a1 1 0 0 1 .293.707V14a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V2a2 2 0 0 1 2-2zm5.5 1.5v2a1 1 0 0 0 1 1h2l-3-3zM4.165 13.668c.09.18.23.343.438.419.207.075.412.04.58-.03.318-.13.635-.436.926-.786.333-.401.683-.927 1.021-1.51a11.651 11.651 0 0 1 1.997-.406c.3.383.61.713.91.95.28.22.603.403.934.417a.856.856 0 0 0 .51-.138c.155-.101.27-.247.354-.416.09-.181.145-.37.138-.563a.844.844 0 0 0-.2-.518c-.226-.27-.596-.4-.96-.465a5.76 5.76 0 0 0-1.335-.05 10.954 10.954 0 0 1-.98-1.686c.25-.66.437-1.284.52-1.794.036-.218.055-.426.048-.614a1.238 1.238 0 0 0-.127-.538.7.7 0 0 0-.477-.365c-.202-.043-.41 0-.601.077-.377.15-.576.47-.651.823-.073.34-.04.736.046 1.136.088.406.238.848.43 1.295a19.697 19.697 0 0 1-1.062 2.227 7.662 7.662 0 0 0-1.482.645c-.37.22-.699.48-.897.787-.21.326-.275.714-.08 1.103z"/>
    </svg>
    </a>
</div>

<br>

&nbsp;&nbsp;&nbsp;&nbsp;Calculation of noise cross-correlation functions (NCF) plays an important role in ambient noise imaging which is a vital seismic method to obtain Earth inner structures. To raise the resolution of the imaging results, we need more seismic data for imaging. However, as the size of seismic data increases, the serial algorithm for NCF calculation becomes much more time-consuming. Thus, how to accelerate the NCF calculation becomes a key problem in ambient noise imaging. Based on the analysis of serial algorithm, we proposed a new parallel algorithm for NCF calculation using NVIDIA GPU platform. In addition, we improved reading and writing strategy to reduce I/O consumption. Experimental results on real seismic data show the effectiveness of our method. The parallel program achives about 1861 times speedup.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/HPC_seis/HPC_SEIS_part1and2.png" title="Figure 1" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 1: Calculation flow of serial algorithm
</div>