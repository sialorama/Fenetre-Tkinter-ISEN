># Fenetre-Tkinter-ISEN
>Fenêtre Tkinter permattant de consulter l'ENT sur le site de l'ISEN Brest.
![Screenshot](screnncapture.png)
```python 
from tkinter import *
import webbrowser
def open_channel():
    webbrowser.open_new("https://auth.isen-ouest.fr/cas/login?service=https://web.isen-ouest.fr/uPortal/Login%3FrefUrl%3D%2FuPortal%2Ff%2Fu29l1s7%2Fnormal%2Frender.uP")
#création de la fenetre
window = Tk()
#personnaliser cette fenetre
window.title("Isen Simplon")
window.geometry("720x480")
window.minsize(480, 360)
window.iconbitmap('C:/Users/Sialorama/Google Drive/[Isen]/iconne.ico')
window.config(background='#41A77F')
#inérer une image
width = 500
height = 200
image = PhotoImage(file="C:/Users/Sialorama/Google Drive/[Isen]/isen_logo.png").zoom(35).subsample(32)
Canvas = Canvas(window, width=width, height=height, bg='#41A77F', bd=0, highlightthickness=0)
Canvas.create_image(width/2, height/2, image=image)
Canvas.pack(expand=YES)
#Créer la frame
#relief prend les valeurs flat, groove, raised, ridge, solid, or sunken
frame = Frame(window, bg='#41A77F', bd=1, relief=SUNKEN)
#ajouter du texte
label_title = Label(frame, text="Isen Brest", font=("Courrier", 28), bg='#41A77F', fg='white')
#centrer le titre
label_title.pack(expand=YES)
#sous titre : sub
label_subtitle = Label(frame, text="Année 2020-2021", font=("Courrier", 20), bg='#41A77F', fg='white')
#expend=YES:centrer le titre
# sinon side = TOP/BOTTOM/RIGHT/LEFT
label_subtitle.pack(expand=YES)
#ajouter un bouton
mon_bouton = Button(frame, text="Visiter l'ENT ISEN", font=("courrier", 25), bg='#41A77F', fg='white', command=open_channel)
mon_bouton.pack(expand=YES)
#Ajouter
frame.pack(expand=YES)
# #afficher
window.mainloop()
```
