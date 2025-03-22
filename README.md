# Exercise M09W02: Text to Image Synthesis using DCGAN + BERT

**Sinh hình ảnh từ văn bản hay tổng hợp văn bản thành hình ảnh (Text to Image)** trong đó các mô hình được huấn luyện với:

**- Input:** đoạn văn bản

**- Ouput:** hình ảnh mô tả hoặc chứa các đối tượng được mô tả trong đoạn văn bản

![Pipeline DCGAN](/readme_img/DCGAN.png "AIO 2024")

Mô hình DCGAN gồm 2 mạng là Generator và Discriminator. Trong đó

**- Generator:** Bao gồm các lớp mạng CNN nhận đầu vào là Noise (z) và Text Embedding (e- Biểu diễn của đoạn văn bản đầu vào). Đầu ra của khối Generator là ma trận ảnh được sinh ra G(z, e).

**- Discriminator:** Bao gồm các lớp mạng CNN nhận đầu vào là biểu diễn của ảnh (ảnh thật hoặc ảnh fake được sinh ra từ khối Generator) sau đó kết hợp với Text Embedding để dự đoán ảnh thật hay ảnh fake.

Trong bài tập này, sử dụng BERT để encode đoạn text đầu vào để mô hình có thể hiểu được.