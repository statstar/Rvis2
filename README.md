# 데이터 시각화 2일차

얼굴 인식 코드 예제

if(!require(magick)) install.packages("magick")

if(!require(image.libfacedetection)) install.packages("image.libfacedetection", repos = "https://bnosac.github.io/drat")

library(magick)

library(image.libfacedetection)

image <- image_read("https://www.korea.kr/newsWeb/resources/temp/images/000182/560_4.jpg")

faces <- image_detect_faces(image)

faces

plot(faces, image, border = "red", lwd = 7, col = "white")
