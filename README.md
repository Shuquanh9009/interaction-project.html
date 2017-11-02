<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>

<head>
    <title>p5js Template</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.3/p5.js"></script>
    
    <script>
        var r
        var g
        var b
        var scale
        var size
        var opacity
     
      function setup() {
            createCanvas(800,600);
            r=random(0,255)
            g=random(0,255)
            b=random(0,255)
            
            scale=1
            size=80
            opacity= -20
        }

       function draw() {
        //These are the random color valuables and the background randomly change color
          r=random(0,255)  
          g=random(0,255)
          b=random(0,255)
          background(r,g,b,15) 
          
          
        }
            
        function mouseMoved(){
         //the eyes (big ones)
          noStroke()
         fill (r,g,b,opacity)//coolors for the eyes
         ellipse(mouseX,mouseY,size*scale,size*scale)//left eye
          ellipse(mouseX+80*scale,mouseY,size*scale,size*scale)//right eye
          // the eyeballs or pupils (small dots inside of the eyes), and the mouth
          fill(r-20,g-20,b-20,opacity)//colors for the eyeball and the mouth
          ellipse(mouseX,mouseY,(size-60)*scale,(size-60)*scale)//left eyeball
          ellipse(mouseX+85*scale,mouseY,(size-60)*scale,(size-60)*scale)//right eyeball
          ellipse(mouseX+40*scale,mouseY+50*scale,(size+30)*scale,(size+10)*scale)//mouth
          opacity++
        }
      function keyPressed(){
        // press the up arrow to increase the size of the eyes and the mouth
        // press the down arrow to decrase the size of the eyes and the mouth
        if (keyCode == UP_ARROW) {
          scale=scale+0.5;
        }
        
        if (keyCode == DOWN_ARROW) {
        scale= scale-0.5;
        } 
        
        
        
      }
        

    </script>
</head>

<body>
    <div id="code" class="container-fluid">
        <script src="https://gist-it.appspot.com/github/shuquanh9009/p5js/blob/master/interaction-project.html?footer=0"></script>
    </div>

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
    <script>
        $(window).bind("load", function() {
            $('#code').before($('#defaultCanvas0').remove());
        });
    </script>
</body>


</html>
