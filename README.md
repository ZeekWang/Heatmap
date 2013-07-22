Heatmap


Heatmap JavaScript Library v1.2
  Usage:
    1. Initialize. You need to create a object with these fields: width, height, sigma, radius, context.
      Then, execute heatmap(object).
      For example, 
      	var config = {
  				width: 1000, //width of the canvas
    			height: 800, //height of the canvas
   				sigma: 8, // sigma of Gauss Kernel
   				radius: 60, // raidus of Gauss kernel
  				quality: 4, //1 is the best quality, 
  							//the quality will decrease with the value increase
  							//lower quality means less time consuming					
   				context: $(canvas).getContext('2d')  //the context of the canvas
  			}
  			heatmap(config);
  
  	2. Call heatmap.draw(nodes) to update and render the heatmap,
   		nodes is an array with objects like {x: _x, y: _y}.
  		For example,
  			var nodes = [{x:100, y:20}, {x:400, y:30}, {x:70, y:340}];
  			heatmap.draw(nodes); 
        node can also formed as [{x:100, y:20, count:3}];

  	3. Each time the size of the canvas	is changed, 
   		please call heatmap.setSize(newWidth, newHeight).
  
    4. Use heatmap.fixMaxDensity() or heatmap.releaseMaxDensity() 
   		to fix or release the max density value. You need to execute 
   		fixMaxDensity after drawing and execute releaseMaxDensity before drawing.
  		
AUTHOR: Zeek Wang
Date: 2013/07/22
