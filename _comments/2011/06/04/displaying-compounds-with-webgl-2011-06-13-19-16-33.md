---
date: '2011-06-13 19:16:33'
link: ''
name: "Jordi Vill\xE0-Freixa"
post_id: /2011/06/04/displaying-compounds-with-webgl
---

I am having troubles displaying the molecule. javascript works fine for me, but I cannot see the mol either in wordpress or in a reglar html file I have build adhoc. Maybe I need to change the permissions for the ChemDoodleWeb files, maybe...



Test page 
{% highlight javascript %}
  document.write("" + Date() + "");  var app = new ChemDoodle.TransformCanvas3D("transformBallAndStick", 500, 500);  app.specs.set3DRepresentation("Stick");  app.specs.backgroundColor = "white";
  var molFile = "\n  Marvin  02080816422D          

 14 15  0  0  0  0            999 V2000\n   -0.7145   -0.4125    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0\n   -0.7145    0.4125    0.0000 N   0  0  0  0  0  0  0  0  0  0  0  0\n    0.7145   -0.4125    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0\n    0.7145    0.4125    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0\n    0.0000   -0.8250    0.0000 N   0  0  0  0  0  0  0  0  0  0  0  0\n    0.0000    0.8250    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0\n    1.4992    0.6674    0.0000 N   0  0  0  0  0  0  0  0  0  0  0  0\n    1.4992   -0.6675    0.0000 N   0  0  0  0  0  0  0  0  0  0  0  0\n    1.9841    0.0000    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0\n   -1.4289   -0.8250    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0\n    0.0001    1.6500    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0\n    0.0001   -1.6500    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0\n    1.7541    1.4520    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0\n   -1.4289    0.8250    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0\n 10  1  2  0  0  0  0\n  1  2  1  0  0  0  0\n 14  2  1  0  0  0  0\n  8  3  1  0  0  0  0\n  4  3  2  0  0  0  0\n  7  4  1  0  0  0  0\n  1  5  1  0  0  0  0\n  5  3  1  0  0  0  0\n 12  5  1  0  0  0  0\n  6  2  1  0  0  0  0\n  6  4  1  0  0  0  0\n 11  6  2  0  0  0  0\n  9  7  1  0  0  0  0\n 13  7  1  0  0  0  0\n  9  8  2  0  0  0  0\nM  END\n";  var molecule = ChemDoodle.readMOL(molFile, 1);  app.loadMolecule(molecule);
{% endhighlight %}
