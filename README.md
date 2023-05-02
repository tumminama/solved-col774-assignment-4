Download Link: https://assignmentchef.com/product/solved-col774-assignment-4
<br>
<ol>

 <li><strong>Dataset Links</strong>

  <ul>

   <li><strong>Train Images: </strong><a href="https://owncloud.iitd.ac.in/nextcloud/index.php/s/bpsRreMBSEAZyy7">Link</a></li>

   <li><strong>Train Captions: </strong><a href="https://owncloud.iitd.ac.in/nextcloud/index.php/s/ZiAsmexxADBcb3J">Link</a></li>

   <li><strong>Public Test Images: </strong><a href="https://owncloud.iitd.ac.in/nextcloud/index.php/s/eGZydAwPwrCygen">Link</a></li>

   <li><strong>Public Test Captions: </strong><a href="https://owncloud.iitd.ac.in/nextcloud/index.php/s/8ZoDbDno7aiRBo7">Link</a></li>

   <li><strong>Private Test Images: </strong><em>Coming Soon</em></li>

  </ul></li>

 <li><strong>Non Competitive Part</strong></li>

</ol>

You are given a dataset of images with 5 possible captions for each image. The images are named as image id.jpg where id is the image index. The captions.tsv file contain the captions of all the images, with each line (tab separated) format having image id and the 5 corresponding captions. You will use the Encoder-Decoder architecture for modelling this problem. An encoder is used to encode the input into a vector representation and a decoder is applied on this vector representation to generate the sequence auto-regressively (one word at a time). You have to implement the encoder for the images and a decoder for text captions in this part along with beam search to find the most optimal sequence. You can use this as a starting point.

<ul>

 <li><strong>Encoder</strong>: Design a CNN based encoder that handles the variable sized images.</li>

</ul>

1

<ul>

 <li><strong>Decoder</strong>: Design a RNN / LSTM based decoder which generates the captions given the encoded image input.</li>

 <li><strong>Training Setup</strong>: Use cross-entropy as the loss function and <a href="https://machinelearningmastery.com/teacher-forcing-for-recurrent-neural-networks/">teacher-forcing</a> for training the decoder. Don’t forget to use START and END tokens to allow variable length caption outputs in the decoder.</li>

 <li><strong>Inference at test time</strong>: Instead of using the token with maximum probability at each step (Greedy Decoding) for generating the tokens (words) in the caption, you will use Beam Search for generating your captions. It is a Dynamic Programming method to get better sequences than simple Greedy Decoding. Read Section 4 of <a href="https://web.stanford.edu/class/cs224n/readings/cs224n-2019-notes06-NMT_seq2seq_attention.pdf">this pdf document</a><a href="https://web.stanford.edu/class/cs224n/readings/cs224n-2019-notes06-NMT_seq2seq_attention.pdf">.</a> We also recommended you to read Sections 1.2, 1.3, and 1.4 for better understanding.</li>

 <li><strong>Evaluation: </strong>You have to generate the top-5 captions for each image using Beam Search as described above. We will use BLEU (BiLingual Evaluation Understudy) scores for evaluating your model performance. You can read more about it in Section 5.3 of <a href="https://web.stanford.edu/class/cs224n/readings/cs224n-2019-notes06-NMT_seq2seq_attention.pdf">this pdf document</a><a href="https://web.stanford.edu/class/cs224n/readings/cs224n-2019-notes06-NMT_seq2seq_attention.pdf">.</a></li>

</ul>

<ol start="3">

 <li><strong>Reference</strong></li>

</ol>

You can refer to <a href="https://arxiv.org/pdf/1411.4555.pdf">this paper</a> to get an in-depth understanding of Image Captioning Encoder-Decoder framework. We also provide the boiler plate code with base classes to make it easier to implement the assignment. You can download it from <a href="http://www.cse.iitd.ac.in/~cs5150286/boiler_plate_code.ipynb">this link</a><a href="http://www.cse.iitd.ac.in/~cs5150286/boiler_plate_code.ipynb">.</a>

<ol start="4">

 <li><strong>Competitive Part</strong>

  <ul>

   <li>Instructions <em>coming soon</em>.</li>

  </ul></li>

 <li><strong>Submission Instructions</strong></li>

</ol>

Make .tsv files [EntryNumber1] [EntryNumber2] [TYPE].tsv similar to test captions.tsv for each of the test sets (TYPE = public/private). Submit these 2 files along with your code and report in a single zip format. Only <strong>one of you </strong>should make the submission.