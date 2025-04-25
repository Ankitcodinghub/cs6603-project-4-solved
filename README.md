# cs6603-project-4-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/cs6603-ai-ethics-and-society-solved-4/

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;121789&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS6603 Project #4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">
            
<div class="kksr-stars">
    
<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
    
<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>
                

<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
Homework Project #4

Readings:

● Chapter 7: Weapons of Math Destruction (Sweating Bullets: On the Job)

● “A Few Useful Things to Know about Machine Learning” by Pedro Domingos https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf

In this assignment, you’ll apply AI/ML algorithms related to two applications – word embeddings and facial recognition.

Task Set #1: Here you will use distributional vectors trained using Google’s deep learning Word2vec system.

(http://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-theircompositionality.pdf). To learn more about the system and how to train your own vectors, you can find more information here (https://code.google.com/archive/p/word2vec). To learn about the python wrapper around Word2vec, you can find more information here (https://raretechnologies.com/word2vec-tutorial/)

2. Install Gensim (Example: pip install gensim. | pip install –upgrade gensim)

3. Download the provided reducedvector.bin file on Canvas which is a a pre-trained Word2vec model based on the Google News dataset (https://code.google.com/archive/p/word2vec/) from gensim.models import Word2Vec import gensim.models

import nltk

newmodel = gensim.models.KeyedVectors.load_word2vec_format(&lt;path to reducedvector.bin&gt;, binary=True)

4. We can compute similarity measures associated with words within the model. For example, to find different measures of similarity based on the data in the Word2vec model, we can use:

# Find the five nearest neighbors to the word man newmodel.most_similar(‘man’, topn=5)

# Compute a measure of similarity between woman and man newmodel.similarity(‘woman’, ‘man’)

5. To complete analogies like man is to woman as king is to ??, we can use:

newmodel.most_similar(positive=[‘king’, ‘woman’], negative=[‘man’], topn=1)

Q1: We will use the target words – man and woman. Use the pre-trained word2vec model to rank the following 15 words from the most similar to the least similar to each target word. For each word-target word pair, provide the similarity score. Provide your results in table format.

wife husband

child queen king man woman

nurse is to hospital as teacher is to ___? usa is to pizza as japan is to ___? human is to house as dog is to ___? grass is to green as sky is to ___? video is to cassette as computer is to ____? universe is to planet as house is to ____? poverty is to wealth as sickness is to ___?

a. Complete the above sentences with your own word analogies. Use the Word2Vec model to find the similarity measure between your pair of words. Provide your results.

Example:

man is to woman as king is to _queen__?

newmodel.similarity(‘king’, ‘queen’) -&gt; 0.5685571

b. Use the Word2Vec model to find the word analogy and corresponding similarity score. Provide

your results.

Example:

man is to woman as king is to ___?

newmodel.most_similar(positive=[‘king’, ‘woman’], negative=[‘man’], topn=1) -&gt; queen, 0.711

c. Lastly, compute and print the correlation between the vector of similarity scores from your analogies versus the Word2Vec analogy-generated similarity scores. What is the strength of the correlation?

o .00-.19 “very weak” correlation o .20-.39 “weak” correlation o .40-.59 “moderate” correlation o .60-.79 “strong” correlation

o .80-1.0 “very strong” correlation

Task Set #2: For this part of the assignment, we will work with the UTK dataset

(UTKface_cropped.tar.gz) available on Canvas and based on the original UTKFace dataset

(https://susanqq.github.io/UTKFace/)

Q1: Each image in the dataset has a unique value representing age, gender, and race based on the following legend:

● age: indicates the age of the person in the picture and can range from 0 to 116.

● gender: indicates the gender of the person and is either 0 (male) or 1 (female).

● race: indicates the race of the person and can from 0 to 4, denoting White, Black, Asian, Indian, and Others (like Hispanic, Latino, Middle Eastern).

Complete and answer the following:

• Compute and document the frequency of images associated with each subgroup for age

(subdivide based on – (0-20), (21,40), (41,60), (61,80), (81, 116)), gender (0,1), and race (0 to 4).

• For age, which subgroup has the largest representation? Which subgroup has the least representation?

• For gender, which subgroup has the largest representation? Which subgroup has the least representation?

• For race, which subgroup has the largest representation? Which subgroup has the least representation?

• Based on what you’ve learned so far, if an algorithm is trained based on this dataset, which group(s) will be impacted the most? Explain why.

Turn in a report (in PDF format) documenting your outputs in each Step. The report should follow the JDF format. Jupyter notebook (ipynb files) submission is optional, but a final PDF document per JDF format is required. The file name for submission is GTuserName_Assignment_4, for example, Joyner03_Assignment_4. Reports that are not neat and well organized will receive up to a 10-point deduction. All charts, graphs, and tables should be generated in Python or Excel, or any other suitable software application, else appropriate points will be deducted, which could be the maximum.
