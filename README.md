# <b>EGG CLASSIFICATION AI MODEL</b>
Code repository made by PhD student Matheus Pupp de Araujo Rosa (Poultry Science Department, Auburn University) for the Final Project from the COMP6600 - Artificial Intelligence class from Auburn University. <br>
<br>
## <b>Dataset</b> <br>
Kindly given by Moreno et al. (Sánchez, J. M. P., Moreno, L. A. O., Rodríguez, J. L. R., & Corro, I. D. M. (2023). Poultry Egg Classification System Using Deep Learning (pp. 1–6). 2023 5th International Congress on Human-Computer Interaction, Optimization and Robotic Applications (HORA). IEEE. https://doi.org/10.1109/HORA58378.2023.10156776). contains approximately 1500 egg images separeted in four different categories (Healthy, Dirty, Cracked, Cracked and Dirty). All credit goes to them and their incredible work on their paper. If you want to reproduce the codes and use their dataset, please refer to them as cited before and send them an email (emails from the team are in the paper).<br>
Dataset was used from the Google Drive. Link for the datatset: https://drive.google.com/drive/folders/1_I_6aZV-rPI21XS-nJEmta-X36oGvlek?usp=drive_link<br>
<br>
## <b>Environment</b> <br>
All codes were run in the Google Colab environment with GPU accelaration. <br>
<br>
## <b>Rationale</b> <br>
The eggshell is one of the main  barriers to keep contamination out of the egg, so the presence of cracks on it open up a possible path to the exterior bacteria to get inside and risk the embryo development. Egg classification is made in order to minimize contamination problems when incubating dirty eggs or litter eggs, incubating them separately. But even with very well trained professionals it is easy to don't see eggs with small cracks and not accounting for them can bring a risk if incubated with clean eggs. <br>
It was recently attempted to use deep learning to classify eggs by many authors, and they seemed successful in their tasks. Thinking about it, and using the information of the paper "Poultry Egg Classification System Using Deep Learning" by Moreno et al., I tried to implement a AI model to account for this egg classification problems in the poultry industry. <br>
<br>
## <b>Implementation</b> <br>
All codes were generrated by ChatGPT and troubleshooted using Gemini AI tools. <br>
### <b>Base model</b> <br>
<b>Pre-process:</b> <br>
<li>Img. Size = 224 </li><br>
<li>Batch size = 64 </li><br>
<b>Base VGG19:</b> <br>
<li>Pre-trained on ImageNet </li><br>
<li>Learning rate = 0.00001 </li><br>
<li>Loss function = categorical crossentropy </li><br>
<li>Optimizer = Adam </li><br>
<b>Evaluation parameters:</b><br>
<li>Precision = exactness </li><br>
<li>Recall = completeness </li><br>
<li>F1-score = balance </li><br>
<b>Overfitting:</b> <br>
<li>Training and Validation accuracy/loss </li><br>
<li>Training = 10 epochs, weighted classes </li><br>
### <b>Fine-Tuning (unfrozen 8 last layers)</b><br>
<li>Recompiled the model </li><br>
<li>Learning rate = 0.00001 </li><br>
<li>Loss = categorical cross-entropy </li><br>
<li>Metrics = accuracy </li><br>
<li>Training = 5 epochs </li><br>
<li>The rest = base model </li><br>
<br>
## REFERENCES <br>
<li>Sánchez, J. M. P., Moreno, L. A. O., Rodríguez, J. L. R., & Corro, I. D. M. (2023). Poultry Egg Classification System Using Deep Learning (pp. 1–6). 2023 5th International Congress on Human-Computer Interaction, Optimization and Robotic Applications (HORA). IEEE. https://doi.org/10.1109/HORA58378.2023.10156776 <br></li>

<li>Dunkley C. S. A Dozen Egg Abnormalities: HOW THEY AFFECT EGG QUALITY, UGA Cooperative Extension Circular 1255, April 2022. Available at: < https://secure.caes.uga.edu/extension/publications/files/pdf/C%201255_1.PDF> <br></li>

<li>Simonyan K., Zisserman A. VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE RECOGNITION, Published as a conference paper at ICLR, 2015. https://doi.org/10.48550/arXiv.1409.1556. <br></li>

<li>Victor Massaki Nakaguchi, R.M. Rasika D. Abeyrathna, Tofael Ahamed. Development of a new grading system for quail eggs using a deep learning-based machine vision system, Computers and Electronics in Agriculture, Volume 226, 2024, 109433, ISSN 0168-1699. https://doi.org/10.1016/j.compag.2024.109433. <br></li>

<li>Çelik A., Tekin El. Classification of Hatchery Eggs Using a Machine Learning Algorithm Based on Image Processing Methods: A Comparative Study, Brazilian Journal of Poultry Science, e-ISSN: 1806-9061 2024 / v.26 / n.2 / 001-012. http://dx.doi.org/10.1590/1806-9061-2023-1882.<br> </li>

<li>KHABISI, M. M, SALAHI, A, & MOUSAVI, S. N (2012). The influence of egg shell crack types on hatchability and chick quality. Turkish Journal of Veterinary & Animal Sciences 36 (3): 289-295. https://doi.org/10.3906/vet-1103-20 <br></li>

<li>Modi, P. Convolutional Neural Networks for Dummies, Medium, 2023. Available at: https://medium.com/@prathammodi001/convolutional-neural-networks-for-dummies-a-step-by-step-cnn-tutorial-e68f464d608f. Accessed: 07/23/2025. </li> 
