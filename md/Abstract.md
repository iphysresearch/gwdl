---
Title:   摘要
Summary: Abstract
Authors: He Wang
Date:    May 30, 2020
blank-value:
some_url: https://example.com
---

</br>

---

## 摘要

</br>

随着 LIGO 在近些年来的观测和发展，引力波 (gravitational wave, GW) 天文学已经迎来了全新的时代。大力发展对引力波波源信号及其电磁对应体 (electromagnetic, EM) 等信使的实时探测技术，其背后的巨大发展潜力将会为基础物理研究催生出重大科学发现。无论是基于模板还是非模板搜寻的引力波信号，其振荡幅度都有着远低于引力波背景噪声的特点。所以，在更广泛意义上对引力波信号的挖掘、分类以及实现高效的波源参数估计等数据分析方法，都将会对实时的多信使天文学 (multimessenger astrophysics, MMA)  的发展有着重要的研究意义。此外，对于引力波数据中广泛存在的反常非高斯噪声实例 (glitch) 的辨别和分类，以及将其与引力波信号区分开来也是另一个具有挑战性的重要研究方向。

目前，性能最佳的引力波数据分析流水线都受限于模板匹配方法所带来的巨大计算开销，因此，很难在引力波波源信号所对应的高维参数空间内进行大范围的实时搜寻。引力波信号精确的数值模拟方法对事件波源的参数估计是至关重要的，但这也很难满足实际的探测需求，这需要覆盖更加完备的波源参数空间，如考虑偏心率和双星自旋等等。对于没有理论模板的引力波信号更是还没有足够有效且灵敏的搜寻办法。此外，对于非稳态且非高斯的引力波探测器噪声数据而言，现行的引力波探测流水线并不是理论上最佳的信号搜索方法。这意味着会有相当数量的真实引力波事件会被漏报。

本论文的研究目标就是通过深度学习 (deep learning, DL) 技术——一个基于人工神经网络 (artificial neural networks, ANN) 的机器学习 (machine learning, ML) 方法——来解决上述研究难题。我们将通过基于深度学习算法的 AI 技术，充分发挥现代硬件架构(如GPUs)的优势，提升对引力波数据的信号处理和数据分析的能力，从而有望发现和理解理论预期之外的引力波信号和波源信息，进而推动实时的引力波天文学和多信使天文学的发展。本论文的主体由七章构成。第[一](C1.md)章绪论，我们概述了引力波天文学和多信使天文学的研究现状。考虑到相关研究的深入所面临的机遇与挑战，我们总结了基于深度学习技术在解决这些研究难题上所具有的天然优势。本论文的论述结构是以第[二](C2.md)、[三](C3.md)章的理论作为铺垫，简明扼要地介绍本论文中所涉及相关技术的原理和方法，并且结合对这一新兴交叉科学领域的理解认识与个人心得，为我们后续的第[四](C4.md)、[五](C5.md)、[六](C6.md)章的主要工作和理论引述打下坚实的论据基础。

在第[二](C2.md)章中，我们将会概述引力波探测及其相关的数据分析理论。引力波探测是一个多学科交叉、多领域合作的科学实验项目。总体而言，可以分为引力波波源的理论建模、引力波探测的实验设计和引力波的数据处理等三大方面。我们会较为详细地介绍与引力波数据分析密切相关的基本概念和常见的处理方法，并且会着重对匹配滤波技术的统计原理和数学细节做详细地介绍。

第[三](C3.md)章我们将会对针对本论文所涉及的深度学习技术和机器学习方法进行详细地阐述。我们会先从一般意义上的角度对机器学习技术的优化原理以及模型性能评估方法出发，通过数据驱动对实现算法优化的过程有一个宏观的认识。再进一步地，以深度神经网络算法作为基本的模型构造，结合对神经元等结构组件的理解，直观地说明人工神经网络的基本构成和相关的深度学习方法。最后，我们着重讨论了与本论文所相关的卷积神经网络的原理细节及其中不同组件的性能特点。

本论文的第[四](C4.md)章是我们通过构建神经网络模型在引力波信号探测和可解释性分析的初探性研究。通过构建和优化神经网络模型，我们实现了对引力波信号的识别。卷积神经网络作为一种黑箱的机器学习模型，我们将通过可视化的方法来了解其结构内部是如何从噪声中辨识出引力波波形信号的。最后，通过研究引力波数据中不同波形在时域上的分布差异以及对引力波信号识别效果的影响，将有助于为研究者在生成训练数据集和优化网络模型时，提供一个具有一定可解释性和指导意义的神经网络模型训练策略。

在第[五](C5.md)章中，基于模拟的 LIGO 探测器背景噪声环境下，我们探讨了不同研究文献中关于信噪比定义的差异和影响，并且从深度神经网络泛化性能的角度，对采取不同信噪比构造的数据分布差异进行了对比研究。随后，我们针对卷积神经网络的超参数结构进行优化和微调，通过与其他研究者所提出的网络结构进行对比，我们提出了一种更简单且性能更优异的改进版卷积神经网络模型。

第[六](C6.md)章，我们讨论真实的 LIGO 引力波数据上的信号探测方法。目前，绝大多数深度学习技术的研究都在模拟噪声中尝试，都还未考虑到对真实的引力波事件进行探测和识别。而在这一章中，我们通过借鉴匹配滤波技术的优势，提出了全新的“匹配滤波-卷积神经网络” (MFCNN) 模型，实现在真实 LIGO 数据环境下的引力波信号识别。我们也对引力波数据流的信号搜寻策略进行了讨论，并成功地将 MFCNN 模型应用在了真实的 O1 和 O2 数据中。我们的结果证实了 MFCNN 可以在速度提高数个量级的基础上，对一些短噪声源 (如 glitch) 有着非常好的鲁棒性。尤为重要的是，本章的工作是相关研究领域中，首次利用深度学习技术，成功地探测识别 LIGO 和 Virgo 在 O1 和 O2 上所有公开发布并确认的真实引力波事件。

最后一章我们对博士期间的相关研究工作做了一些总结和展望，并对将来的工作提出了设想。


- 关键词: 引力波，数据分析，匹配滤波，卷积神经网络，深度学习，机器学习


</br>

---

## Abstract

</br>

A new era of gravitational wave (GW) astronomy has begun with the recent detections by LIGO. Real-time observations of GW signals and their electromagnetic (EM) and astro-particle counterparts will unlock its full potential for scientific discoveries of fundemental physics. Extracting and classifying the wide range of modeled and unmodeled GW signals, whose amplitudes are often much weaker than the background noise, and rapidly inferring accurate parameters of their source is crucial in enabling this scenario of real-time multimessenger astrophysics. Identifying and automatically distinguishing anomalous non-Gaussian transient noises (glitches) that frequently contaminate the data and separating them from true GW signals is yet another difficult challenge. 

Currently, the most sensitive data analysis pipelines are limited by the extreme computational costs of template-matching methods and thus are unable to scale to all types of GW sources and their full parameter space. Accurate numerical models of GW signals covering the entire range of parameters including eccentric and spin-precessing compact binaries, which are essential to infer the astrophysical parameters of an event, are not available. Searches for unmodeled and anomalous signals do not have sufficient sensitivity compared to the targeted searches. Furthermore, existing search pipelines are not optimal for dealing with the non-stationary, non-Gaussian noise in the detectors. This indicates that many critical events will go unnoticed. 

The primary objective of this thesis is to resolve the above issues via deep learning, a state-of-the-art machine learning method based on artificial neural networks. With the advantage of deep learning techniques and modern computational hardware (such as GPU), we could improve the capabilities for data analysis and signal processing of GW, which will be helpful for further understanding  of the sources of GW signals beyond theoretical expectation and thus promote the development of real-time gravitational wave astronomy and multimessenger astronomy. The main body consists of seven chapters. The first Chapter is the introduction, which introduces the background knowledge related to the author’s two research work. We outline the current status, challenges, and opportunities in gravitational wave astronomy and multimessenger astronomy. To recapitulate, we summarize the strengths of deep learning based approach to solve these challenging tasks. The structure of this dissertation is as follows. Based on the concise description of Chapters 2 and 3, which briefly introduces the principles and methods of related technologies in this dissertation and combines the understanding of this emerging cross-disciplinary fields with personal perception, we could lay a solid foundations for the arguments and citations in our follow-up of the fourth, fifth, and sixth Chapters.

In the Chapter 2, we will outline gravitational wave detection techniques and the related theory of gravitational wave data analysis. Gravitational wave detection is a international scientific research project with multi- and cross-disciplinary collaborations. In general, it can be divided into three major aspects: the theoretical and computational modeling of gravitational wave sources, the experimental design of gravitational wave detection, and the data analysis of gravitational waves. We will introduce in more detail the basic concepts and common processing methods that are closely related to the analysis of gravitational wave data, and will focus on the statistical principles and mathematical details of the matched filtering techniques.

In the Chapter 3, we will elaborate on the deep learning techniques and machine learning methods involved in this thesis. Started with a perspective of the general sense of optimization theory and method of performance evaluation of machine learning model, we will have a macro view of the process of data-driven algorithm optimization. Further, with the deep neural network algorithm used as the basic model constructure, and the understanding of the structural components such as neurons, the basic composition of artificial neural networks and related deep learning methods are intuitively illustrated. Finally, we will focus on the principles of the convolutional neural networks in details related to the thesis and the performance characteristics of different components are discussed.

In the Chapter 4, we have constructed a neural network model in the preliminary exploration of gravitational wave signal detection and interpretability analysis. By optimizing the neural network model, we successfully realized the recognition of gravitational wave signals. Considering the convolutional neural network as a black box of machine learning model, we will know how to identify its internal structure for gravitational wave signal from noise by visualization. Finally, by analyzing the differences in the distribution of different waveforms data in the time domain and the effect on the recognition of gravitational wave signals, we will provide an interpretive and instructive neural network training strategies for generating training data sets and optimizing neural network models.

In the Chapter 5, Based on the simulated background noise environment of the LIGO detector, we will explore the differences and impacts of the definitions and data distributions of signal-to-noise ratio in related research literatures, and from the perspective of the generalization performance of deep neural networks, a comparative study is carried out. Subsequently, we have optimized and fine-tuned the hyperparameters of the convolutional neural network. By comparing with the network structures proposed by other researchers, we will proposed an improved version of the convolutional neural network model that is much simpler and better in performance.

In the Chapter 6, we discuss signal detection methods on real LIGO gravitational wave data. At present, most of the researches on deep learning technology are attempted in the background of simulated noise, and only a few consider detection and identification for the real gravitational wave events. In this chapter, we draw on the advantages of matched filtering techniques and propose a new "matched-filtering convolutional neural network" (MFCNN) model to realize the recognition of gravitational wave signals in the real LIGO data recordings. We also discuss the signal search strategy of the data stream of gravitational wave, and successfully applied the MFCNN model to real O1 and O2 data. Our results confirm that MFCNN can be very robust to short noise sources (such as glitches) on the basis of several orders of magnitude speed improvement. It is particularly noteworthy that the work in this chapter is the first time in related research fields using deep learning technology to successfully detect and identify all the real gravitational wave events published and confirmed by LIGO and Virgo on O1 and O2.

In the last chapter, we reach some conclusions and outlooks based on the related works during my PhD study, and we also propose some picture of our future work.

- Keywords: gravitational waves，data analysis，matched filtering，convolutional neural networks，deep learning，machine learning


