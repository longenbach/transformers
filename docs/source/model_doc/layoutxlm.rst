.. 
    Copyright 2021 The HuggingFace Team. All rights reserved.

    Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with
    the License. You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on
    an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the
    specific language governing permissions and limitations under the License.

LayoutXLM
-----------------------------------------------------------------------------------------------------------------------

Overview
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

LayoutXLM was proposed in `LayoutXLM: Multimodal Pre-training for Multilingual Visually-rich Document Understanding
<https://arxiv.org/abs/2104.08836>`__ by Yiheng Xu, Tengchao Lv, Lei Cui, Guoxin Wang, Yijuan Lu, Dinei Florencio, Cha
Zhang, Furu Wei. It's a multilingual extension of the `LayoutLMv2 model <https://arxiv.org/abs/2012.14740>`__ trained
on 53 languages.

The abstract from the paper is the following:

*Multimodal pre-training with text, layout, and image has achieved SOTA performance for visually-rich document
understanding tasks recently, which demonstrates the great potential for joint learning across different modalities. In
this paper, we present LayoutXLM, a multimodal pre-trained model for multilingual document understanding, which aims to
bridge the language barriers for visually-rich document understanding. To accurately evaluate LayoutXLM, we also
introduce a multilingual form understanding benchmark dataset named XFUN, which includes form understanding samples in
7 languages (Chinese, Japanese, Spanish, French, Italian, German, Portuguese), and key-value pairs are manually labeled
for each language. Experiment results show that the LayoutXLM model has significantly outperformed the existing SOTA
cross-lingual pre-trained models on the XFUN dataset.*

One can directly plug in the weights of LayoutXLM into a LayoutLMv2 model, like so:

.. code-block::

    from transformers import LayoutLMv2Model

    model = LayoutLMv2Model.from_pretrained('microsoft/layoutxlm-base') 

As LayoutXLM's architecture is equivalent to that of LayoutLMv2, one can refer to :doc:`LayoutLMv2's documentation page
<layoutlmv2>` for all tips, code examples and notebooks.

This model was contributed by `nielsr <https://huggingface.co/nielsr>`__. The original code can be found `here
<https://github.com/microsoft/unilm>`__.
