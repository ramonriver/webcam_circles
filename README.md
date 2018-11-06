# webcam_circleis
Circle detection from online webcam images

La transformada HOUGH és una tècnica per extreure característiques en imatges digitals. Tracta de trobar punts distintius a partir dels quals marcar línies, cercles o elipses agrupant-los.

A continuació s'explica el funcionament dels paràmetres que intervenen en la funció que utilitza la transformada HOUGH per detectar cercles:

cv::HoughCircles( gray_image, circles, CV_HOUGH_GRADIENT, HOUGH_ACCUM_RESOLUTION, MIN_CIRCLE_DIST, CANNY_EDGE_TH, HOUGH_ACCUM_TH, MIN_RADIUS, MAX_RADIUS );

const double HOUGH_ACCUM_RESOLUTION = 2;  //resolució a l'hora de determinar que un conjunt de punts són o no cercles
const double MIN_CIRCLE_DIST = 40;        //distància mínima entre centres de cercles detectats
const double CANNY_EDGE_TH = 150;         //llindar superior per a la detecció de cercles
const double HOUGH_ACCUM_TH = 70;         //llindar inferior per a la detecció de cercles (com més petit, més falsos cercles            
                                          //   detectats
const int MIN_RADIUS = 20;                //radi mínim dels cercles considerats
const int MAX_RADIUS = 100;               //radi màxim dels cercles considerats

Referències:
https://en.wikipedia.org/wiki/Hough_transform

https://docs.opencv.org/2.4/modules/imgproc/doc/feature_detection.html?highlight=houghcircles
