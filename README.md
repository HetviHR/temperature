//author: Hetvi Radadiya
//Date: 18/04/2024
#include<iostream>
using namespace std;

class temperature
{
private:
float kelvin;
float celsius;
float fehrenhit;

  
public:
int ch;


float k2c(float kelvin){
    celsius = kelvin - 273.15;
    
    return celsius;
}


float f2c(float fehrenhit)
    {
   celsius = (fehrenhit - 32)*5/9;
   return celsius;  
   }


float k2f(float kelvin)
{
 float temp=   k2c(kelvin);
 fehrenhit = c2f(temp);
    return fehrenhit;
}


float f2k(float fehrenhit){
    float t = f2c(fehrenhit);
    kelvin = c2k(t);
    return kelvin;
}


float c2k(float celcius){
    kelvin = celsius + 273.15;
    return kelvin;
}


float c2f(float celsius)
{
    fehrenhit = (celsius*9/5)+32;
    return fehrenhit;
}

    temperature();
    ~temperature();
};

temperature::temperature()

{
    cout<<"Which temperarure do you want to convert in another two unit??";
    cout<<endl<<"1.celsius" <<endl<<"2.kelvin"<<endl<<"3.fehrenhit"<<endl;
    
cin>>ch;
}

temperature::~temperature()
{
}

int main()
{
  float t;  
    temperature t1;
    switch (t1.ch)
    {
    case 1:
     cout<<endl<<"enter temperature in celcius unit: "<<endl;
     cin>>t;
    cout<<"Fehrenhit = "<<t1.c2f(t)<<endl;
    cout<<"Kelvin = "<<t1.c2k(t)<<endl;
        break;
    
     case 2:
     cout<<endl<<"enter temperature in kelvin unit: "<<endl;
     cin>>t;
    cout<<"Fehrenhit = "<<t1.k2f(t)<<endl;
    cout<<"Celsius = "<<t1.k2c(t)<<endl;
        break;
    
     case 3:
     cout<<endl<<"enter temperature in Fehrenhit unit: "<<endl;
     cin>>t;
    cout<<"Celcius = "<<t1.f2c(t)<<endl;
    cout<<"Kelvin = "<<t1.f2k(t)<<endl;
        break;
    
    default:
    cout<<endl<<"Sorry!! INVALID INPUT YOU HAVE ENTERED!!"<<endl;
        break;
    }
}# temperature
you can change unit of temperature from one to another
