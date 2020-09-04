# A foolproof way to shrink deep learning models
## Researchers unveil a pruning algorithm to make artificial intelligence applications run faster.

### Kim Martineau | MIT Quest for Intelligence
### April 30, 2020

![img](https://news.mit.edu/sites/default/files/styles/news_article__image_gallery/public/images/202004/learning_rate_rewinding.png?itok=gmiKfotm)

As more artificial intelligence applications move to smartphones, deep learning models are getting smaller to allow apps to run faster and save battery power.
Now, MIT researchers have a new and better way to compress models.

It's so simple that they unveiled it [in a tweet][1] last month: Train the model,
prune its weakest connections, retrain the model at its fast, early training rate, and repeat, until the model is as tiny as you want.

"That's it," says [Alex Renda][2], a PhD student at MIT.
"The standard things people do to prune their models are crazy complicated."

Renda discussed the technique when the International Conference of Learning Representation (ICLR) convened remotely this month. 
Renda is a co-author of the work with [Jonathan Frankle][3], a fellow PhD student in MIT's [Department of Electrical Engineering and Computer Science][4] (EECS), 
and [Michael Carbin][5], an assistant professor of electrical engineering and computer science -- all members of the [Computer Science and Artificial Science Laboratory][6].

The search for a better compression technique grew out of Frankle and Carbin's award-winning [Lotter Ticket Hypothesis][7] paper at ICLR last year. 
They showed that a deep neural network could perform with only one-tenth the number of connections if the right subnetwork was found early in training.
Their revelation came as demand for computing power and energy to train ever larger deep learning models was increasing exponentially, 
a trend that continues to this day. Costs of that growth include a rise in planet-warming carbon emissions and a potential drop 
in innovation as researchers not affiliated with big tech companies compete for scarce computing resources.
Everyday usrs are affected, too. Big AI models eat up mobile-phone bandwidth and battery power.

But at a colleague's suggestion, Frankle decided to see what lessons it might hold for pruning, a set of techniques for reducing the size of a neural network by removing unnecessary connections or neurons.
Pruning algorithms had been around for decades, but the field saw a resurgence after the breakout success of neural networks at classifying images in the [ImageNet competition][8].
As models got bigger, with researchers adding on layers of artificial neurons to boost performance, others proposed techniques for whittling them down.

[Song Han][9], now an assistant professor at MIT, was one pioneer. Building on a series of influential papers, Han unveiled a pruning algorithm he called
AMC, or [AutoML for model compression][10], that's still the industry standard. Under Han's technique, 
redundant neurons and connections are automatically removed, and the model is retrained to restore its initial accuracy.

In response to Han's work, Frankle recently suggested in an [unpublished paper][11] that results could be further improved by rewinding the smaller, 
pruned model to its initial parameters, or weights, and retraining the smaller model at its faster, initial rate.

In the current ICLR study, the researchers realized that the model could simply be rewound to its early training rate without fiddling with any parameters.
In any pruning regimen, the tinier a model gets, the less accurate it becomes. But when th researchers compared this new method
to Han's AMC or Frankle's weight-rewinding methods, it performed better no matter how much the model shrank.

It's unclear why the pruning technique works as well as it does. The researchers say they will leave that question for others to answer.
As for those who with to try it, the algorithm is as easy to implement as other pruning methods, without time-consuming tuning, the researchers say.

"It's the pruning algorithm from the 'Book,'" says Frankle. "It's clear, generic, and drop-dead simple."

Han, for this part, has now partly shifted focus from compression AI models to channeling AI to design small, efficient models from the start. 
His newest method, [Once for All][12], also debuts at ICLR. Of the new learning rate method, he says: "I'm happy to see new pruning and retraining techniques evolve,
giving more people access to high-performing AI applications."

Support for the study came from the Defense Advanced Research Projects Agency, Google, MIT-IBM Watson AI Lab, MIT Quest for Intelligence, and the U.S. Office of Naval Research.

Original Text [link][13]

[1]: https://twitter.com/alex_renda_/status/1237393727389184007
[2]: https://alexrenda.com/
[3]: http://www.jfrankle.com/
[4]: https://www.eecs.mit.edu/
[5]: https://www.csail.mit.edu/person/michael-carbin
[6]: https://www.csail.mit.edu/
[7]: https://arxiv.org/pdf/1803.03635.pdf
[8]: https://songhan.mit.edu/
[9]: https://arxiv.org/pdf/1802.03494.pdf
[10]: https://arxiv.org/pdf/1802.03494.pdf
[11]: https://arxiv.org/abs/1803.03635
[12]: http://news.mit.edu/2020/artificial-intelligence-ai-carbon-footprint-0423
[13]: https://news.mit.edu/2020/foolproof-way-shrink-deep-learning-models-0430?fbclid=IwAR06_GqJ4mRd06xUH8WBOCbLiY0ApS1x0lsqoMhA7TUSEyGTAat1oCP1H6Q