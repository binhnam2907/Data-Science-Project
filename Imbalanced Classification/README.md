GG Drive for more information and gg colab: https://drive.google.com/drive/u/2/folders/1-KCu2WQefUnqlNxXp7flZv5jTm88r495

## Overview of project:
  - Project này gồm 2 phần:
    - Phần 1: Gender classification.
    - Phần 2: COVID19 classification.
## Phần 1:
  - Gender Classification Dataset là tập data chứa ảnh gương mặt của nam và nữ (2 classes female và male) đã được chia thành 2 folder train (23000 female samples và 23000 male samples), val (5800 female samples và 5800 male samples). Thực hiện theo các yêu cầu bên dưới để tiến hành phân tích các kỹ thuật đối phó với imbalanced trong task phân loại. (Chọn 1 class là Positive class (Female) và class còn lại là Negative class). Từ yêu cầu 1.2, tạo ra 2 tập data như đã hướng dẫn ở trên là dataset A (loại bỏ positive class chỉ còn 2300 samples) và dataset B (loại bỏ positive class chỉ còn 1000 samples). Dùng tập data 2k3_augment cho yêu câì 1.7 và 1k_augment cho yêu cầu 1.8 và 2k3_50_augment cho yêu cầu 1.11.
      - 1.1 Balanced Classification: Xây dựng pipeline để xử lý và load data cho việc train và validation. Tiêp theo xây dựng 1 classification model tùy ý (ResNet, VGG, ...). Thực hiện train và đánh giá kết quả phân loại Positive và Negative class của model
      - 1.2 Imbalanced Classes: Dùng model ở bước yêu cầu 1.1 để train với dataset A.
      - 1.3 Heavy Imbalanced Classes: Dùng model ở bước yêu cầu 1.1 để train với dataset B
      - 1.4 Class Weights: Dùng kỹ thuật Class Weight để train và model ở bước yêu cầu 1.1 để train với dataset A
      - 1.5 Class Weights: Dùng kỹ thuật Class Weight để train và model ở bước yêu cầu 1.1 để train với dataset B
      - 1.5 Undersampling: Dùng kỹ thuật Undersampling để train và model ở bước yêu cầu 1.1 để train với dataset A
      - 1.6 Undersampling: Dùng kỹ thuật Undersampling để train và model ở bước yêu cầu 1.1 để rain với dataset B
      - 1.7 Oversampling: Dùng kỹ thuật Oversampling để train và model ở bước yêu cầu 1.1 để train ới dataset A
      - 1.8 Oversampling: Dùng kỹ thuật Oversampling để train và model ở bước yêu cầu 1.1 để train ới dataset B
      - 1.9 Focal Loss: Dùng Focal Loss để train và model ở bước yêu cầu 1.1 để train với dataset A.
      - 1.10 Focal Loss: Dùng Focal Loss để train và model ở bước yêu cầu 1.1 để train với dataset B.
      - 1.11 Combination: Tìm cách kết hợp những kỹ thuật ở trên hoặc kiến thức đã được học trước đó hoặc kỹ thuật mới để train với tập data set (A hoặc B tùy ý). Gợi ý: oversampling nhưng chỉ giới hạn Positive samples = 50% Negative samples sau đó kết hợp ới focal loss để train.
      - 1.12 Comparison: So sánh các kết quả đã train từ các model áp dụng những kỹ thuật chống lại ấn đề imbalance

## Phần 2:
  - Covid19 X-ray Images Classification là 1 phần từ tập dataset thật của đại học Qatar University gồm các ảnh phổi X-ray thể hiện một người có bị nhiễm covid 19 hay không (2 classes COVID và NORMAL). Tập train có 586 COVID image và 9192 NORMAL image và tập val có 1000 COVID image và 1000 NORMAL image.
      - Baseline Model: Xây dựng pipeline để xử lý và load data cho việc train và validation. Tiêp theo xây dựng 1 classification model tùy ý (ResNet, VGG, ...). Thực hiện train và đánh giá kết quả phân loại ảnh phổi có bị nhiễm COVID.
      - 5 Techniques to Deal with Imbalanced Classes: lựa chọn 5 kỹ thuật phù hợp với dataset này để giảm thiểu ảnh hưởng của vấn đề imbalance trong dataset. Có thể thử nghiệm với pretrained model.
