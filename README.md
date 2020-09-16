# John-Whitney-Assignment-1

#include "ofApp.h"

//--------------------------------------------------------------
void ofApp::setup(){

}

//--------------------------------------------------------------
void ofApp::update(){

}

//--------------------------------------------------------------
void ofApp::draw(){
    
    ofSetBackgroundColor(0, 0, 0);
    ofSetLineWidth(2);
    ofSetColor(255);
    ofNoFill();
    
    
    for (int i = 0; i < 16; i++){
            
            float time = ofGetElapsedTimef();
            float t = pow(time, 2);
        
        //size of original triangle
            float scaler = 10;
            float radius = i * scaler;
        
        //phase
            float phase = ofMap(i, 0, 19, -1, 1);
        
        //frequency
            float f = ofMap(i, 0, 19, 20, 20 + radius * 0.5);
        
        
            float originx1 = 0.5 * ofGetWidth();
            float originx2 = 0.5 * ofGetWidth();
            float originy1 = 0.5 * ofGetWidth();
            float originy2 = 0.5 * ofGetWidth();
    
        
            
            float shiftax = radius * sin(-120 * PI / 180);
            float shiftay = radius * cos(-120 * PI / 180);
            float shiftbx = radius * sin(-240 * PI / 180);
            float shiftby = radius * cos(-240 * PI / 180);
            float shiftcx = radius * sin(0 * PI / 180);
            float shiftcy = radius * cos(0 * PI / 180);

            float start1xa = originx1 + shiftax;
            float start1ya = originy1 + shiftay;
            float start1xb = originx1 + shiftbx;
            float start1yb = originy1 + shiftby;
            float start1xc = originx1 + shiftcx;
            float start1yc = originy1 + shiftcy;
            float start2xa = originx2 + shiftax;
            float start2ya = originy2 + shiftay;
            float start2xb = originx2 + shiftbx;
            float start2yb = originy2 + shiftby;
            float start2xc = originx2 + shiftcx;
            float start2yc = originy2 + shiftcy;
            
            
            
        
        float scalarrotate = 100;
            float timescaler = 0.001;
            
        
        float speed =  ofMap(i, 0, 19, 20, 20 + radius * 0.5);
        
            float rotatex = - scalarrotate * cos( f * timescaler * t );
            float rotatey = - scalarrotate * sin( f * timescaler * t );
            float eclipses = 0.75;
            
            
            float p1x = start1xa + rotatex;
            float p1y = start1ya - eclipses * rotatey;
            float p2x = start1xb + rotatex;
            float p2y = start1yb - eclipses * rotatey;
            float p3x = start1xc + rotatex;
            float p3y = start1yc - eclipses * rotatey;
            float p4x = start2xa - rotatex;
            float p4y = start2ya - eclipses * rotatey;
            float p5x = start2xb - rotatex;
            float p5y = start2yb - eclipses * rotatey;
            float p6x = start2xc - rotatex;
            float p6y = start2yc - eclipses * rotatey;
    
        
            ofDrawTriangle(p1x, p1y, p2x, p2y, p3x, p3y);
            ofDrawTriangle(p4x, p4y, p5x, p5y, p6x, p6y);
        
        
            
            

            
        
    
    }
    
}

//--------------------------------------------------------------
void ofApp::keyPressed(int key){

}

//--------------------------------------------------------------
void ofApp::keyReleased(int key){

}

//--------------------------------------------------------------
void ofApp::mouseMoved(int x, int y ){

}

//--------------------------------------------------------------
void ofApp::mouseDragged(int x, int y, int button){

}

//--------------------------------------------------------------
void ofApp::mousePressed(int x, int y, int button){

}

//--------------------------------------------------------------
void ofApp::mouseReleased(int x, int y, int button){

}

//--------------------------------------------------------------
void ofApp::mouseEntered(int x, int y){

}

//--------------------------------------------------------------
void ofApp::mouseExited(int x, int y){

}

//--------------------------------------------------------------
void ofApp::windowResized(int w, int h){

}

//--------------------------------------------------------------
void ofApp::gotMessage(ofMessage msg){

}

//--------------------------------------------------------------
void ofApp::dragEvent(ofDragInfo dragInfo){ 

}
