A comparative analysis of multiple deep learning architectures — VGG16, AlexNet, GoogLeNet, RNN, and CNN — trained and evaluated on benchmark datasets MNIST and CIFAR-10. The project investigates the effect of different train-test splits and analyzes each model’s performance using metrics like accuracy, confusion matrix, ROC curve, and AUC.

Quick Summary of performance

==================== Performance Comparison on MNIST ====================
                                    test_loss  test_accuracy
AlexNet (Simple) (Val Split 10%)     0.022809         0.9921
AlexNet (Simple) (Val Split 20%)     0.026478         0.9911
GoogLeNet (Simple) (Val Split 10%)   0.035066         0.9885
GoogLeNet (Simple) (Val Split 20%)   0.035241         0.9887
RNN (LSTM) (Val Split 10%)           0.071020         0.9809
RNN (LSTM) (Val Split 20%)           0.065692         0.9809
VGG (Simple) (Val Split 10%)         0.019945         0.9937
VGG (Simple) (Val Split 20%)         0.019748         0.9942



==================== Performance Comparison on CIFAR10 ====================
                            test_loss  test_accuracy
AlexNet (Val Split 10%)      0.812362         0.7879
AlexNet (Val Split 20%)      1.008787         0.7647
GoogLeNet (Val Split 10%)    0.623932         0.7941
GoogLeNet (Val Split 20%)    0.624876         0.7903
RNN (LSTM) (Val Split 10%)   1.214281         0.5842
RNN (LSTM) (Val Split 20%)   1.206890         0.5753
VGG-16 (Val Split 10%)       1.087513         0.6212
VGG-16 (Val Split 20%)       1.094925         0.6198





