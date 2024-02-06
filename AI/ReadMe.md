# To Update Current AI Trends..
:hugs:[Hugging Face](https://huggingface.co/) </br>
:page_with_curl:[PapersWithCode](https://paperswithcode.com/) </br>

# Dataset
:art:[AI Hub](https://www.aihub.or.kr/)

# Useful Codes
```python
# unseen tf GPU use warning
import os
os.environ['TF_CPP_MIN_LOG_LEVEL']='2'
```

# Model Evaluation
### Evaluation
```python
model.compile(..., metrics=[...])
history = model.fit(...)
score = model.evaluate(...) # print metrics values
```

### Loss-Epoch plot
```python
plot_loss(history):
plt.plot(history.history['loss'])
plt.plot(history.history['val_loss'])
plt.title('Model loss')
plt.ylabel('Loss')
plt.xlabel('Epoch')
plt.legend(['train', 'val'], loc='upper right')
plt.show()
```

### ROC Curve
```python
from sklearn.metrics import roc_curve, roc_auc_score

probs = model.predict(x_test, verbose=0)[:,1]

auc = roc_auc_score(y_test.values, probs)
fpr, tpr, _ = roc_curve(y_test.values, probs)

plt.plot(fpr, tpr)
plt.title('CNN ROC Curve (AUC = ' + str(round(auc,4)) + ')')
plt.xlabel('False Positive Rate')
plt.ylabel('True Positive Rate')
plt.show()
```

### Precision-Recall Curve

`formula` 
> $Precision = \frac{TP}{(TP + FP)}$ </br>
> $Recall = \frac{TP}{(TP + FN)}$

```python
from sklearn.metrics import auc
probs = model.predict(x_test, verbose=0)[:,1]
precision, recall, thresholds = precision_recall_curve(y_test.values, probs)
  
pr_auc = auc(recall, precision)
plt.plot(recall, precision)
  
plt.title('CNN Precision-Recall Curve (AUC = ' + str(round(pr_auc,4)) + ')')
plt.xlabel('Recall')
plt.ylabel('Precision')
plt.show()
```

### Computer Vision Evaluation Metrics
##### Peak Signal-to-noise ratio (PSNR) 
##### Structural Similarity Index Map (SSIM) 
##### Learned Perceptual Image Patch Similarity(LPIPS)

# MultiGPU processing

![image](https://github.com/mj0410/SomethingUseful/assets/66175878/60a27319-a739-4c14-81d8-e81e7c3f1f28)
