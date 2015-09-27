var sketchProc = function(processingInstance) {
					with(processingInstance) {
										size(1580, 600);
										frameRate(30);

										// ProgramCodeGoesHere
										var magnifyer = function(x,y,w,h) {
    var i=get(mouseX/2,mouseY/1.3,w,h);
    image(i,width-width,height-h);
    noFill();
    stroke(0,0,0);
    strokeWeight(3);
    rect(width-width,height-h,w,h);
};
var draw = function() {
    background(98, 255, 0);
    fill(0, 26, 255);
    ellipse(100,100,100,100);
    magnifyer(0,299,100,100);
};
}}; // Get the canvas that Processing-js will use
var canvas = document.getElementById("mycanvas");
// Pass the function sketchProc (defined in myCode.js) to Processing's constructor.
var processingInstance = new Processing(canvas, sketchProc);
