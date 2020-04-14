# Socialdataanalysis2020 - Plan and structure for final project


* An explanation of the central idea behind your final project (what is the idea? which datasets do you need to explore the idea?, why is it interesting?)

Preliminary investigation and exploration of New York led to the discovery of several interesting datasets. The first a 


* A mock up of the visualization that you wish to build. (Anything is fine here. Pen and paper, MS Paint, Inkscape, D3, anything.).





## Make sure you answer the questions
* What genre is it? (for Genres, see section 4.3 of the Segel and Heer paper)

The story we want to convey will be realized through multiple genres. There will be supporting texts to visualizations which is a form of the magazine style.
Additionally there will be annotated charts and flow charts to direct the story. 


* Why is that genre right for telling the story you want to communicate with the data

The main genre is magazine style. Here there is a linear way of directing the reader by text and vizualisations to support the written text. 
In this way the story is presented clearly, moving from point to point guiding the reader, 

* An outline on the elements you'll need to get to your goal.
- blabla


## The implementation plan.
- 


### A walk-through of your preliminary data-analysis, addressing
* What is the total size of your data? (MB, number of rows, number of variables, etc)


* What are other properties? (What is the date range? Is is it geo-data?, then a quick plot of locations, etc.)


* Show the fundamental distributions of the data (similar to the work we did on SF crime data for lecture 3)
<!DOCTYPE html>
<html lang="en">
  
  <head>
    
      <meta charset="utf-8">
      <title>Bokeh Plot</title>
      
      
        
          
        
        
          
        <script type="text/javascript" src="https://cdn.bokeh.org/bokeh/release/bokeh-2.0.0.min.js" integrity="sha384-5Y+xuMRAbgBj/2WKUiL8yzV4fBFic1HJPo2hT3pq2IsEzbsJjj8kT2i0b1lZ7C2N" crossorigin="anonymous"></script>
        <script type="text/javascript">
            Bokeh.set_log_level("info");
        </script>
        
      
      
    
  </head>
  
  
  <body>
    
      
        
          
          
            
              <div class="bk-root" id="ed3b19be-579a-49d8-a3d4-b84aa5517e1e" data-root-id="5314"></div>
            
          
        
      
      
        <script type="application/json" id="5562">
          {"2e4cd084-e722-4326-a9ec-b2552911a857":{"roots":{"references":[{"attributes":{"api_key":"AIzaSyBuYWAMFD8WHiaL7BJwntptaPh3HilIuxs","below":[{"id":"5323"}],"left":[{"id":"5328"}],"map_options":{"id":"5312"},"renderers":[{"id":"5344"}],"title":{"id":"5315"},"toolbar":{"id":"5335"},"x_range":{"id":"5316"},"x_scale":{"id":"5452"},"y_range":{"id":"5317"},"y_scale":{"id":"5451"}},"id":"5314","subtype":"GMap","type":"GMapPlot"},{"attributes":{"source":{"id":"5340"}},"id":"5345","type":"CDSView"},{"attributes":{},"id":"5454","type":"Selection"},{"attributes":{},"id":"5333","type":"ResetTool"},{"attributes":{},"id":"5316","type":"Range1d"},{"attributes":{},"id":"5451","type":"LinearScale"},{"attributes":{"formatter":{"id":"5326"},"ticker":{"id":"5327"}},"id":"5328","type":"LinearAxis"},{"attributes":{"dimension":"lat"},"id":"5327","type":"MercatorTicker"},{"attributes":{"lat":30.2861,"lng":-97.7394,"zoom":11},"id":"5312","type":"GMapOptions"},{"attributes":{"fill_alpha":{"value":0.8},"fill_color":{"value":"blue"},"line_color":{"value":"#1f77b4"},"size":{"units":"screen","value":15},"x":{"field":"lon"},"y":{"field":"lat"}},"id":"5342","type":"Circle"},{"attributes":{},"id":"5317","type":"Range1d"},{"attributes":{"active_drag":"auto","active_inspect":"auto","active_multi":null,"active_scroll":"auto","active_tap":"auto","tools":[{"id":"5331"},{"id":"5332"},{"id":"5333"},{"id":"5334"}]},"id":"5335","type":"Toolbar"},{"attributes":{},"id":"5452","type":"LinearScale"},{"attributes":{"dimension":"lon"},"id":"5321","type":"MercatorTickFormatter"},{"attributes":{},"id":"5331","type":"PanTool"},{"attributes":{},"id":"5332","type":"WheelZoomTool"},{"attributes":{"data":{"lat":[30.29,30.2,30.29],"lon":[-97.7,-97.74,-97.78]},"selected":{"id":"5454"},"selection_policy":{"id":"5455"}},"id":"5340","type":"ColumnDataSource"},{"attributes":{"dimension":"lon"},"id":"5322","type":"MercatorTicker"},{"attributes":{"text":"Austin"},"id":"5315","type":"Title"},{"attributes":{},"id":"5455","type":"UnionRenderers"},{"attributes":{},"id":"5334","type":"HelpTool"},{"attributes":{"dimension":"lat"},"id":"5326","type":"MercatorTickFormatter"},{"attributes":{"formatter":{"id":"5321"},"ticker":{"id":"5322"}},"id":"5323","type":"LinearAxis"},{"attributes":{"data_source":{"id":"5340"},"glyph":{"id":"5342"},"hover_glyph":null,"muted_glyph":null,"nonselection_glyph":{"id":"5343"},"selection_glyph":null,"view":{"id":"5345"}},"id":"5344","type":"GlyphRenderer"},{"attributes":{"fill_alpha":{"value":0.1},"fill_color":{"value":"blue"},"line_alpha":{"value":0.1},"line_color":{"value":"#1f77b4"},"size":{"units":"screen","value":15},"x":{"field":"lon"},"y":{"field":"lat"}},"id":"5343","type":"Circle"}],"root_ids":["5314"]},"title":"Bokeh Application","version":"2.0.0"}}
        </script>
        <script type="text/javascript">
          (function() {
            var fn = function() {
              Bokeh.safely(function() {
                (function(root) {
                  function embed_document(root) {
                    
                  var docs_json = document.getElementById('5562').textContent;
                  var render_items = [{"docid":"2e4cd084-e722-4326-a9ec-b2552911a857","root_ids":["5314"],"roots":{"5314":"ed3b19be-579a-49d8-a3d4-b84aa5517e1e"}}];
                  root.Bokeh.embed.embed_items(docs_json, render_items);
                
                  }
                  if (root.Bokeh !== undefined) {
                    embed_document(root);
                  } else {
                    var attempts = 0;
                    var timer = setInterval(function(root) {
                      if (root.Bokeh !== undefined) {
                        clearInterval(timer);
                        embed_document(root);
                      } else {
                        attempts++;
                        if (attempts > 100) {
                          clearInterval(timer);
                          console.log("Bokeh: ERROR: Unable to run BokehJS code because BokehJS library is missing");
                        }
                      }
                    }, 10, root)
                  }
                })(window);
              });
            };
            if (document.readyState != "loading") fn();
            else document.addEventListener("DOMContentLoaded", fn);
          })();
        </script>
    
  </body>
  
</html>

