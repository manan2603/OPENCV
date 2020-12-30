# OPENCV
//This is my first program on OpenCV and this program detects face in an image


    import cv2
    face_cascade= cv2.CascadeClassifier("haarcascade_frontalface_default.xml")

    img= cv2.imread("image1.jpeg", 1)
    gray_img= cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)

    faces= face_cascade.detectMultiScale(gray_img, 1.1,5)

    print(type(faces))
    print(faces)

    for (x,y,w,h) in faces:
        img=cv2.rectangle(img, (x,y), (x+w,y+h), (0,255,0), 3)

        cv2.imshow("image1.jpeg", img)
        cv2.waitKey()
