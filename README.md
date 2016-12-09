# webcam_point_feature
Detection of ORB features from online webcam imges.

Links consultats:

https://en.wikipedia.org/wiki/Oriented_FAST_and_rotated_BRIEF

http://docs.opencv.org/3.0-beta/doc/py_tutorials/py_feature2d/py_orb/py_orb.html

http://docs.opencv.org/3.0-beta/doc/py_tutorials/py_feature2d/py_matcher/py_matcher.html

http://www.willowgarage.com/sites/default/files/orb_final.pdf


Un detector ORB, és bàsicament la fusiò d’un detector de punts (FAST) i un descriptor (BRIEF), modificats pertinentment, el primer filtre ens millora el temps de càlcul i el segon ens facilita els càlculs.

El filtre FAST detecta cantonades, però  aplicant el filtre de Harris, elimina l’excès de punts donant uns resultats més acurats. 
El filtre BRIEF, es un descriptor que fa tests binaris entre pixels, aquest filtre es molt estable a les distorsions de les prespectives, als canvis de llum I als difuminats, però molt sensible a la rotació.

Per evitar la sensiblilitat a la rotació ORB ho ha solventat gràcies a  un efectiu sistema d’orientació anomenat “intensitat del centroide”, en la qual  es considera que la intensitat que genera una cantonada es equidistant del seu centre, I aquest vector és el que ens indicarà la direcció.
