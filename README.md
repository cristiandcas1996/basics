##EJERJCIO LEDS
## Cuantos leds debo usar para el aviso de los leds, la entrada debe ser la cantidad de numeros 
## Ademas de cual numero se va a poner en el aviso  
ledds=[]
class leds:
    num_leds={ 
    "0": 6,
    "1": 2,
    "2": 5,
    "3": 5,
    "4": 4,                  ##DON'T FORGOT COMMAS
    "5": 5,
    "6": 6,
    "7": 3,
    "8": 7,
    "9": 6,
     }
    
    def __init__(self, numero):
        self.numero= numero
        
    def numero_leds(self):
        Leds=0
               
        for x in self.numero:
           Leds+=self.num_leds[x]
           ledds.append(Leds)        
        return "{} cantidad de leds ". format(Leds)

def total_leds(ledds):
    total=0
    for k in ledds:
        total+=k
    return "El total de leds es: {} ".format(total)
        

        
  
n= int(input("Ingrese la cantidad de numeros: ")) 

for i in range(n):
    numero= input("Ingrese numero: ")             ##SI le dejo el int() no me deja llamrlo despues 
    led1=leds(numero)
    print(led1.numero_leds())
print(total_leds(ledds))    
    
    

    ## darle el valor de los leds para el numero de manera que me vaya sumando para despues retorn cantidad
