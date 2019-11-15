FROM jarzamendia/alpine-glibc-2.29-r0:3.9

#Install Depends
RUN apk add --update --no-cache cairo fontconfig glib icu-libs leptonica libgcc libgomp libstdc++ musl pango curl \
     && apk add --update --no-cache tesseract-ocr \
     && cd /usr/share/tessdata \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/tessdata_best/master/osd.traineddata \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/tessdata_best/master/por.traineddata \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/tessdata_best/master/eng.traineddata \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/desired_characters \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/por.numbers \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/por.punc \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/por.training_text \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/por.training_text.bigram_freqs \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/por.training_text.unigram_freqs \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/por.unicharambigs \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/por.word.bigrams \
     && curl -O https://raw.githubusercontent.com/tesseract-ocr/langdata/master/por/por.wordlist \
     && chmod -R 755 /usr/share/tessdata \
     && LANG=pt_BR.UTF-8

ARG BUILD_DATE

# Labels.
LABEL org.label-schema.schema-version="1.0"
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.name="cosmiccube"
LABEL org.label-schema.description="Imagem com o CosmicCube"
LABEL org.label-schema.url="https://opensource.google.com/projects/tesseract"
LABEL org.label-schema.vendor="Tesseract OCR"
LABEL org.label-schema.version="1"