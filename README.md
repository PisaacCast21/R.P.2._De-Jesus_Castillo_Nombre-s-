# R.P.2._De-Jesus_Castillo_Pedro-Isaac
# ejemplo 1 importar wx

app = wx.App (clearSigInt = True) # clearSigInt para permitir la terminación del programa con CTRL + C frame = wx.Frame (parent = None, title = "") ## main window object panel = wx.Panel (parent = frame ) text = wx.StaticText (parent = panel, label = "Hola, desde wxPython !!", pos = (40,50)) frame.Show () app.MainLoop ()
![image](https://user-images.githubusercontent.com/79875930/112524973-07161380-8d66-11eb-82bd-d11e5e7ed7ba.png)



# ejemplo 2 import wx import webbrowse

clase MyApp (wx.App): def init (self): super (). init (clearSigInt = True)
    # marco de inicio
    self.InitFrame ()
    
def InitFrame (propio):
    frame = MyFrame (parent = None, title = "Basic Frame", pos = (100, 100))
    frame.Show (Verdadero)
class MyFrame (wx.Frame): # subclase de wx.Window; El marco es una ventana de nivel superior # Un marco es una ventana cuyo tamaño y posición pueden (normalmente) ser cambiados por el usuario. # Por lo general, representa la primera ventana principal que verá un usuario def init (self, parent, title, pos = pos): super (). Init (parent = parent, title = title, pos = pos)
def OnInit (self):
    panel = MyPanel (padre = yo)
   
   ![image](https://user-images.githubusercontent.com/79875930/112525071-214ff180-8d66-11eb-9558-f97823fbd446.png)

   
# ejemplo 3 import wx import webbrowser


clase MyApp (wx.App): def init (self): super (). init (clearSigInt = True)
    # marco de inicio
    self.InitFrame ()

def InitFrame (propio):
    frame = MyFrame (parent = None, title = "my button app", pos = (100, 100))


    frame.Show ()
class MyFrame (wx.Frame): # subclase de wx.Window; El marco es una ventana de nivel superior # Un marco es una ventana cuyo tamaño y posición pueden (normalmente) ser cambiados por el usuario. # Por lo general, representa la primera ventana / principal que verá un usuario def init (self, parent, title, pos): super (). Init (parent = parent, title = title, pos = pos) self.OnInit ()

def OnInit (self):
    panel = MyPanel (padre = yo)
class MyPanel (wx.Panel): # Un panel es una ventana en la que se colocan los controles. (por ejemplo, botones y cuadros de texto) # La clase wx.Panel generalmente se coloca dentro de un objeto wxFrame. Esta clase también se hereda de la clase wxWindow. def init (propio, padre): super (). init (padre = padre)
    # agregar un mensaje de saludo al panel
    welcomeText = wx.StaticText (self, label = "¡Para aprender wxPython, haga clic en el enlace de abajo!", pos = (20,20))
    # agregar un botón para abrir el cuadro de diálogo
    button = wx.Button (parent = self, label = 'Click Here!', pos = (20, 120))
    button.Bind (wx.EVT_BUTTON, self.onSubmit) # vincular acción al botón
def onSubmit (self, event):
    # cosas para hacer con el botón de enviar
    webbrowser.open ('https://wxpython.org/Phoenix/docs/html/index.html')
    
if name == "main": app = MyApp () app.MainLoop () 

![image](https://user-images.githubusercontent.com/79875930/112525130-2f057700-8d66-11eb-833b-4404f9823f34.png)
![image](https://user-images.githubusercontent.com/79875930/112525208-43e20a80-8d66-11eb-9da6-e73d2be7ae24.png)


# ejemplo 4 import wx


clase MyApp (wx.App): def init (self): super (). init ()
def OnInit (self):
    frame = MyFrame (parent = None, title = "Este es un marco")
    frame.Show ()
    volver verdadero
class MyFrame (wx.Frame): # subclase de wx.Window; El marco es una ventana de nivel superior # Un marco es una ventana cuyo tamaño y posición pueden (normalmente) ser cambiados por el usuario. # Por lo general, representa la primera ventana / principal que verá un usuario def init (self, parent, title): super (). Init (parent = parent, title = title, pos = (100, 100))
    self.OnInit ()
def OnInit (self):
    panel = MyPanel (propio)
class MyPanel (wx.Panel): # Un panel es una ventana en la que se colocan los controles. (por ejemplo, botones y cuadros de texto) # La clase wx.Panel generalmente se coloca dentro de un objeto wxFrame. Esta clase también se hereda de la clase wxWindow. def init (self, parent): super (). init (parent = parent) self._dont_show = False # para el cuadro de diálogo del mensaje
    # agregar un mensaje de saludo al panel
    welcomeText = wx.StaticText (self, label = "¡Hola mundo!", pos = (20,20)
    
    
     # agregar un cuadro de texto
    self._text = wx.TextCtrl (parent = self, value = 'INGRESE ALGUN TEXTO AQUÍ', pos = (20,60), size = (300, 50))
    # agregar un botón para abrir el cuadro de diálogo![image](https://user-images.githubusercontent.com/79875930/112525146-3462c180-8d66-11eb-8533-4f7ee19fbdc0.png)


    self._buton = wx.Button (parent = self, label = 'Submit', pos = (20, 120))
def ShowDialog (self):
    # ¡Aparece una ventana de diálogo de mensaje al enviar!
    si self._dont_show:
        regresar Ninguno
    dlg = wx.RichMessageDialog (padre = Ninguno, 
            message = "¿Estás listo para aprender wxPython?",
            título = "wxPythonStuff",
            estilo = wx.YES_NO | wx.CANCEL | wx.CENTRE)
    dlg.ShowCheckBox ("No mostrar esto de nuevo")
    dlg.ShowModal () # muestra el diálogo
    si dlg.IsCheckBoxChecked ():
        print ("¿Está marcada la casilla de verificación?", dlg.IsCheckBoxChecked ())
        self._dont_show = Verdadero
def onSubmit (self, event):
    # cosas para hacer con el botón de enviar
    imprimir (self._text.GetValue ())
    self.ShowDialog ()
si nombre == "principal":
aplicación = MyApp ()
frame = MyFrame (parent = None, title = "Este es un marco")
app.MainLoop ()

![image](https://user-images.githubusercontent.com/79875930/112525384-7429a900-8d66-11eb-889a-7259b15690ef.png)

![image](https://user-images.githubusercontent.com/79875930/112525412-7b50b700-8d66-11eb-8eac-3ff05b71404a.png)

# ejemplo 5 importar wx


clase MyApp (wx.App): def init (self): super (). init (clearSigInt = True)
    # marco de inicio
    self.InitFrame ()
def InitFrame (propio):
    marco = MyFrame ()
    frame.Show ()
class MyFrame (wx.Frame): def init (self, title = "MyButtonApp", pos = (100,100)): super (). init (None, title = title, pos = pos) # inicializar el contenido del marco self.OnInit ()
def OnInit (self):
    self.panel = mi_panel (self)
    self.Fit ()
clase mi_panel (wx.Panel):
def __init__ (yo, padre):
    súper(). __init__ (padre = padre)
    # Agregue un panel para que se vea correcto en todas las plataformas
    # art proveedor proporciona arte básico https://wxpython.org/Phoenix/docs/html/wx.ArtProvider.html
    bmp = wx.ArtProvider.GetBitmap (id = wx.ART_INFORMATION, 
    cliente = wx.ART_OTHER, tamaño = (16, 16))
    titleIco = wx.StaticBitmap (self, wx.ID_ANY, bmp)
    title = wx.StaticText (self, wx.ID_ANY, 'Mi título')
    inputOneIco = wx.StaticBitmap (self, wx.ID_ANY, bmp)
    labelOne = wx.StaticText (self, wx.ID_ANY, 'Entrada 1')
    self.inputTxtOne = wx.TextCtrl (self, wx.ID_ANY, value = 'Cuadro de texto')
    inputTwoIco = wx.StaticBitmap (self, wx.ID_ANY, bmp)
    labelTwo = wx.StaticText (self, wx.ID_ANY, 'Entrada 2')
    # wx.SpinCtrl combina wx.TextCtrl y wx.SpinButton en un control.
    self.inputTwo = wx.SpinCtrl (self, wx.ID_ANY, valor = "0", min = 0, max = 100)
    inputThreeIco = wx.StaticBitmap (self, wx.ID_ANY, bmp)
    labelThree = wx.StaticText (self, wx.ID_ANY, 'Entrada 3')
    self.inputThree = wx.Choice (self, elecciones = ['A', 'B', 'C'])
    
inputFourIco = wx.StaticBitmap (self, wx.ID_ANY, bmp)
    labelFour = wx.StaticText (self, wx.ID_ANY, 'Entrada 4')
    self.inputFour1 = wx.CheckBox (parent = self, label = "Opción 1")
    self.inputFour2 = wx.CheckBox (parent = self, label = "Opción 2")
    self.inputFour3 = wx.CheckBox (parent = self, label = "Opción 3")
    okBtn = wx.Button (self, wx.ID_ANY, 'OK')
    cancelBtn = wx.Button (self, wx.ID_ANY, 'Cancelar')
    self.Bind (wx.EVT_BUTTON, self.onOK, okBtn)
    self.Bind (wx.EVT_BUTTON, self.onCancel, cancelBtn)
    mainSizer = wx.BoxSizer (wx.VERTICAL)
    titleSizer = wx.BoxSizer (wx.HORIZONTAL)
    inputOneSizer = wx.BoxSizer (wx.HORIZONTAL)
    inputTwoSizer = wx.BoxSizer (wx.HORIZONTAL)
    inputThreeSizer = wx.BoxSizer (wx.HORIZONTAL)
    inputFourSizer = wx.BoxSizer (wx.HORIZONTAL)
    submitBtnSizer = wx.BoxSizer (wx.HORIZONTAL)
    titleSizer.Add (titleIco, 0, wx.ALL, 5)
    titleSizer.Add (título, 0, wx.ALL, 5)
    inputOneSizer.Add (inputOneIco, 0, wx.ALL, 5)
    inputOneSizer.Add (labelOne, 0, wx.ALL, 5)
    inputOneSizer.Add (self.inputTxtOne, 1, wx.ALL | wx.EXPAND, 5)
    inputTwoSizer.Add (inputTwoIco, 0, wx.ALL, 5)
    inputTwoSizer.Add (labelTwo, 0, wx.ALL, 5)
    inputTwoSizer.Add (self.inputTwo, 1, wx.ALL | wx.EXPAND, 5)
    inputThreeSizer.Add (inputThreeIco, 0, wx.ALL, 5)
    inputThreeSizer.Add (labelThree, 0, wx.ALL, 5)
    inputThreeSizer.Add (self.inputThree, 1, wx.ALL | wx.EXPAND, 5)
    inputFourSizer.Add (inputFourIco, 0, wx.ALL, 5)
    inputFourSizer.Add (labelFour, 0, wx.ALL, 5)
    inputFourSizer.Add (self.inputFour1, 1, wx.ALL | wx.EXPAND, 5)
    inputFourSizer.Add (self.inputFour2, 1, wx.ALL | wx.EXPAND, 5)
    inputFourSizer.Add (self.inputFour3, 1, wx.ALL | wx.EXPAND, 5)
    submitBtnSizer.Add (okBtn, 0, wx.ALL, 5)
    submitBtnSizer.Add (cancelBtn, 0, wx.ALL, 5)
    mainSizer.Add (titleSizer, 0, wx.CENTER)
    mainSizer.Add (wx.StaticLine (self,), 0, wx.ALL | wx.EXPAND, 5)
    mainSizer.Add (inputOneSizer, 0, wx.ALL | wx.EXPAND, 5)
    mainSizer.Add (inputTwoSizer, 0, wx.ALL | wx.EXPAND, 5)
    mainSizer.Add (inputThreeSizer, 0, wx.ALL | wx.EXPAND, 5)
    mainSizer.Add (inputFourSizer, 0, wx.ALL | wx.EXPAND, 5)
    mainSizer.Add (wx.StaticLine (propio), 0, wx.ALL | wx.EXPAND, 5)
    mainSizer.Add (submitBtnSizer, 0, wx.ALL | wx.CENTER, 5)
    self.SetSizer (mainSizer)
    mainSizer.Fit (auto)
    self.Layout ()
def onOK (yo, evento):
    # Hacer algo
    print ('controlador onOK')
    datos = self.getData ()
    imprimir (datos)
def onCancel (self, event):
    self.closeProgram ()
def closeProgram (self):
    # self.GetParent () obtendrá el marco que
    # tiene el método .Close () para cerrar el programa
    self.GetParent (). Close ()
def getData (self):
    '' '
    esto aquí obtendrá datos de todos los botones
    '' '
    datos = []
    data.append (self.inputTxtOne.GetValue ())
    data.append (self.inputTwo.GetValue ())
    selección = self.inputThree.GetSelection ()
    data.append ((selección, 
                self.inputThree.GetString (selección))
                )
    data.append (self.inputFour1.GetValue ())
    data.append (self.inputFour2.GetValue ())
    data.append (self.inputFour3.GetValue ())
    devolver datos
Ejecuta el programa
if nombre == 'principal': aplicación = MyApp () app.MainLoop ()
![image](https://user-images.githubusercontent.com/79875930/112525466-89063c80-8d66-11eb-8d9a-17ec2d9989fa.png)

![image](https://user-images.githubusercontent.com/79875930/112525495-8efc1d80-8d66-11eb-89d5-c37fac50324e.png)

