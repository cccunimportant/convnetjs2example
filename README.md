# ConvNetJs2 -- Convolution neural network suite

Language: [English](README.md) | [中文版](chineseReadme.md)

ConvNetJs2 is a continuation of [ConvNetJS](https://github.com/karpathy/convnetjs) project!

[ConvNetJS] is a JavaScript Convolutional Neural Network project created by [Karpathy](https://github.com/karpathy).

# Examples 

Example | program | description
--------|-----|--------------------------------
Regression | [regression.js](regression) | USES x*sin(x) curve to generate some samples, and then USES CNN to learn the curve that conforms to these samples as far as possible
2D-Classification | [classified2d.js](classified2d.js) | there are two points on the 2-dimensional plane. The two points are distinguished as far as possible by CNN network
MNIST | [mnist](mnist/) | MNIST digital imaging database can be used to train CNN networks to recognize handwritten Numbers
CiFar10 | [cifar10](cifar10/) | Cifar10 image database contains ten categories of tagged objects that are used to train CNN networks for identification (this example USES pre-trained networks to predict).

## Installation


```
$npm -i convnetjs2
```

Then you may run the following example!

## Run 

Example: [regression.js](regression.js)  (curve fitting)

Run

```
$ node regression

x=-1.9028 label=1.7989
x=3.8790 label=-2.6082
x=4.6815 label=-4.6792
x=-4.6472 label=-4.6373
x=-0.6499 label=0.3933
x=1.5464 label=1.5459
x=-1.5151 label=1.5128
x=-4.9869 label=-4.8002
x=4.6274 label=-4.6107
x=-4.7968 label=-4.7797
x=2.0379 label=1.8196
x=-0.3359 label=0.1107
x=-1.7841 label=1.7437
x=0.1969 label=0.0385
x=3.4417 label=-1.0176
x=-2.1675 label=1.7929
x=-3.0291 label=0.3400
x=3.6663 label=-1.8368
x=4.1647 label=-3.5555
x=-1.2591 label=1.1984
0: avloss = 9.948295937040514
1: avloss = 6.205032224246171
2: avloss = 4.675939634667663
3: avloss = 3.25463524477676
4: avloss = 2.056740359677689
5: avloss = 1.2210661058526135
6: avloss = 0.7613773901091525
7: avloss = 0.5294579238376026
8: avloss = 0.411712483449666
9: avloss = 0.34082247976352853
...
96: avloss = 0.04294753998296066
97: avloss = 0.042818343549592436
98: avloss = 0.042691171206738876
99: avloss = 0.04256638734313586
============predicts============
x=-1.9028 label=1.7989 predict=1.7917
x=3.8790 label=-2.6082 predict=-2.7259
x=4.6815 label=-4.6792 predict=-4.8665
x=-4.6472 label=-4.6373 predict=-4.4928
x=-0.6499 label=0.3933 predict=0.4278
x=1.5464 label=1.5459 predict=1.5027
x=-1.5151 label=1.5128 predict=1.4845
x=-4.9869 label=-4.8002 predict=-4.9466
x=4.6274 label=-4.6107 predict=-4.7495
x=-4.7968 label=-4.7797 predict=-4.7121
x=2.0379 label=1.8196 predict=1.7758
x=-0.3359 label=0.1107 predict=0.1073
x=-1.7841 label=1.7437 predict=1.7427
x=0.1969 label=0.0385 predict=0.0613
x=3.4417 label=-1.0176 predict=-1.2772
x=-2.1675 label=1.7929 predict=1.7986
x=-3.0291 label=0.3400 predict=0.3285
x=3.6663 label=-1.8368 predict=-2.0350
x=4.1647 label=-3.5555 predict=-3.5837
x=-1.2591 label=1.1984 predict=1.1957
```


Example: [classified2d.js](classified2d.js) (two-dimensional classification)

Run:

```
$ node classified2d
0: avloss = 0.6926390656268775
1: avloss = 0.6079319150639381
2: avloss = 0.544738413662955
3: avloss = 0.4960600790068934
4: avloss = 0.4568650617104245
5: avloss = 0.4239681925366754
6: avloss = 0.3954026492236949
7: avloss = 0.36991470239945023
8: avloss = 0.34665083097033145
...
96: avloss = 0.016158735032651795
97: avloss = 0.015959671235881746
98: avloss = 0.015765543569039663
99: avloss = 0.015576178731016032
x=-0.4326 y=1.1909 label=1 w0=0.0043 w1=0.9957
x=3.0000 y=4 label=1 w0=0.0188 w1=0.9812
x=0.1253 y=-0.0376 label=1 w0=0.0084 w1=0.9916
x=0.2877 y=0.3273 label=1 w0=0.0139 w1=0.9861
x=-1.1465 y=0.1746 label=1 w0=0.0024 w1=0.9976
x=1.8133 y=1.0139 label=0 w0=0.9782 w1=0.0218
x=2.7258 y=1.0668 label=0 w0=0.9880 w1=0.0120
x=1.4117 y=0.5593 label=0 w0=0.9703 w1=0.0297
x=4.1832 y=0.3044 label=0 w0=0.9892 w1=0.0108
x=1.8636 y=0.1677 label=0 w0=0.9837 w1=0.0163
x=0.5000 y=3.2 label=1 w0=0.0090 w1=0.9910
x=0.8000 y=3.2 label=1 w0=0.0092 w1=0.9908
x=1.0000 y=-2.2 label=1 w0=0.0297 w1=0.9703
```

Example: [mnist/mnistPredict.js](mnist/mnistPredict.js) (MNIST Handwritten digit recognition)

Run

```
$ node mnistPredict mnist/3.png
prob = {"sx":1,"sy":1,"depth":10,"w":{"0":0.000010923343930336934,"1":6.92728679933889e-8,"2
":0.0023810993989678117,"3":0.9745521665891758,"4":1.8340081483249712e-7,"5":0.0230457305123
80742,"6":0.0000034610106813664274,"7":0.0000018766610333963584,"8":0.0000033616660795228394
,"9":0.0000011281440682443508}}
yhat=3 class=3

$ node mnistPredict mnist/2.png
prob = {"sx":1,"sy":1,"depth":10,"w":{"0":0.0010535738445952624,"1":1.1990893606721855e-8,"2
":0.00027351140341995086,"3":0.0006070421170483321,"4":0.000001476107822754898,"5":0.0625423
5834857638,"6":1.5880431439373823e-7,"7":0.9342859563103688,"8":0.0006515079930608026,"9":0.
0005844030798995669}}
yhat=7 class=7

$ node mnistPredict mnist/5.png
prob = {"sx":1,"sy":1,"depth":10,"w":{"0":0.009062010637839395,"1":0.000020162466540627157,"
2":0.0104861679391416,"3":0.009956732504541047,"4":0.000006336915105310351,"5":0.96803134024
76854,"6":0.0004724523803393561,"7":0.0016217035681368212,"8":0.00026114428908309627,"9":0.0
0008194905158701984}}
yhat=5 class=5

$ node mnistPredict mnist/4.png
prob = {"sx":1,"sy":1,"depth":10,"w":{"0":0.028692523186077575,"1":5.02205736407436e-9,"2":0
.07484723060778124,"3":0.00006464052188511926,"4":0.7821497035942716,"5":0.00270130829780131
2,"6":0.11140825235536667,"7":0.00000276406585927267,"8":0.00008180864642785416,"9":0.000051
76370247194745}}
yhat=4 class=4
```

Example: [cifar10/cifar10predict.js](cifar10/cifar10predict.js) (Image Recognition)

Run


```
$ node cifar10predict cifar10/horse1.png
prob = {"sx":1,"sy":1,"depth":10,"w":{"0":0.0016191668416885175,"1":0.000012028667443401294,
"2":0.00042730552373016205,"3":0.00945259560059607,"4":0.04008810208195672,"5":0.00353869245
13365046,"6":0.0000444488262784924,"7":0.9446988432571785,"8":0.00001403701234182708,"9":0.0
0010477973744988698}}
yhat=7 class=horse

$ node cifar10predict cifar10/cat1.png
prob = {"sx":1,"sy":1,"depth":10,"w":{"0":0.0003985102369045928,"1":3.437716650950919e-7,"2"
:0.011440874029435015,"3":0.6484472087027208,"4":0.11506053677703139,"5":0.19549242547893048
,"6":0.00012934290600129334,"7":0.028992669050050313,"8":0.00002642396533101553,"9":0.000011
665081930143968}}
yhat=3 class=cat

$ node cifar10predict cifar10/frog1.png
prob = {"sx":1,"sy":1,"depth":10,"w":{"0":0.00003421294931794948,"1":0.000017947038770644535
,"2":0.033605270574590874,"3":0.006853134039534868,"4":0.010987703276430564,"5":0.0033318320
674363988,"6":0.9449662927777916,"7":0.0001895019112482015,"8":0.0000019482396542533928,"9":
0.000012157125224625852}}
yhat=6 class=frog
```
