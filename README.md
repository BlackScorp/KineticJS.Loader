#KineticJS.Loader

Loader Plugin for KineticJS Canvas Framework

#Installation

* Include file after kinetic.js in HTML
    <script src="https://raw.github.com/BlackScorp/KineticJS.Loader/master/Loader.js"></script>

* Download Loader.js into KineticJS/plugins , update thorfile, create new KineticJS version
* Add the Loader as git submodule , update thorfile, create new KineticJS custom version
    git submodule add https://github.com/BlackScorp/KineticJS.Loader.git src/plugins/BlackScorp

#Usage
    var images = {id:"image1",src:"test.png",
                  id:"image2",src:"test.png"  }
                  
    var loader = new Kinetic.Plugin.Loader(images);
    //Function called after each loaded image
    loader.onProgress(function(loaded,total,percent,src,name){
    
    });
    //Function called after each error on loading
    loader.onError(function(loaded,total,percent,src,name){
    
    });
    //Function called after complete loading
    loader.onComplete(function(loaded,total,percent,src,name){
    
    });
    //Start loading
    loader.load();
    //Getting the loaded images somewhere in other Files
    var image = Kinetic.Global.Assets.image1; 
    //or
    var image = Kinetic.Global.Assets["image1"];