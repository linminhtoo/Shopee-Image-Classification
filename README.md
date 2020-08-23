# Shopee-Image-Classification
Notebook detailing my approach to rank Top 2% out of ~900 teams during the Image Classification segment of the Shopee Code Leage 2020, achieving 83% top-1 accuracy. This was a challenging competition where we were given barely 2 weeks, plus the dataset had problems like many wrong labels, nonsense images and imbalanced classes. <b> This was my first Computer Vision competition, and I learnt fast.ai from scratch during this competition, so time was tight, but I am very happy with what I achieved </b>. I used a pretrained EfficientNet-B4 with a variety of SOTA augmentation techniques and a couple of training tricks to push the accuracy. 

I tried my best to explain the most important techniques I used. Still, some details are omitted for conciseness. I tried many things during the competition and learnt a lot. Feel free to <a href="https://www.linkedin.com/in/minhtoo/">reach out to me on LinkedIn</a> for a discussion, or perhaps to collaborate on an AI project! 

<b>Note: images do not load properly on GitHub</b>. Please download and view the .ipynb file on Jupyter Notebook. 
I also thank my teammate, Benjamin Chew, for kickstarting the initial fast.ai experiments and exposing me to the beauty of fast.ai!! 

## Things I would have loved to try (also discussed within the notebook)
- In the last few days, it was increasingly clear that it was important to classify the text-based images correctly. A human would recognise that a particular screenshot of an SMS was talking about XXX product (say a laptop), and hence, belonged in the laptops category. I had an idea of using an open-source OCR to extract text from such images, and use some form of simple NLP model with word embeddings or even just MLP to extract a feature vector. Concatenating this text-based feature with the image features should yield a nontrivial performance boost. Due to time constraints, I did not manage to try it out. After the challenge ended, I saw a Kaggle notebook showing this, so it will definitely be in my repertoire in future. 
- Kaggle TPUs (but needs tensorflow; fast.ai doesn't support TPUs out of the box)

## References
1. https://github.com/fastai/fastai 
9. https://github.com/oguiza/fastai_extensions
2. https://mila.quebec/wp-content/uploads/2019/08/2009_curriculum_icml.pdf Bengio, Yoshua, et al. "Curriculum learning." Proceedings of the 26th annual international conference on machine learning. 2009.
3. https://arxiv.org/abs/1906.02629 Müller, Rafael, Simon Kornblith, and Geoffrey E. Hinton. "When does label smoothing help?." Advances in Neural Information Processing Systems. 2019.
4. https://arxiv.org/abs/1502.01852 He, Kaiming, et al. "Delving deep into rectifiers: Surpassing human-level performance on imagenet classification." Proceedings of the IEEE international conference on computer vision. 2015.
6. https://arxiv.org/pdf/1910.00762 Jiang, Angela H., et al. "Accelerating deep learning by focusing on the biggest losers." arXiv preprint arXiv:1910.00762 (2019).
7. https://arxiv.org/abs/2002.08973 Gontijo-Lopes, Raphael, et al. "Affinity and Diversity: Quantifying Mechanisms of Data Augmentation." arXiv preprint arXiv:2002.08973 (2020).
8. https://arxiv.org/abs/1710.03740 Micikevicius, Paulius, et al. "Mixed precision training." arXiv preprint arXiv:1710.03740 (2017).
9. http://proceedings.mlr.press/v95/takahashi18a.html Takahashi, Ryo, Takashi Matsubara, and Kuniaki Uehara. "Ricap: Random image cropping and patching data augmentation for deep cnns." Asian Conference on Machine Learning. 2018.
10. https://arxiv.org/abs/1710.09412 Zhang, Hongyi, et al. "mixup: Beyond empirical risk minimization." arXiv preprint arXiv:1710.09412 (2017).
11. https://openaccess.thecvf.com/content_ICCV_2019/html/Yun_CutMix_Regularization_Strategy_to_Train_Strong_Classifiers_With_Localizable_Features_ICCV_2019_paper.html Yun, Sangdoo, et al. "Cutmix: Regularization strategy to train strong classifiers with localizable features." Proceedings of the IEEE International Conference on Computer Vision. 2019.
5. https://towardsdatascience.com/weight-initialization-in-neural-networks-a-journey-from-the-basics-to-kaiming-954fb9b47c79
10. https://towardsdatascience.com/boost-your-cnn-image-classifier-performance-with-progressive-resizing-in-keras-a7d96da06e20
