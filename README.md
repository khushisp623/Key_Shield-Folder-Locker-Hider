import os
import shutil
old=input("Enter the dir of folder to protect : ");
new=input("Enter new the file name : ");
pwd=input("Enter the password : ");
new_folder="C:/Users/Lenovo/Desktop"
#x=new_folder
new_folder=os.path.join(new_folder,new)
os.mkdir(new_folder)
for i in pwd:
    for j in range(0,10):
        path=os.path.join(new_folder,str(j))
        try:
            os.mkdir(path)
        except:
            pass
        for k in range(0,10):
            path2=os.path.join(path,str(k))
            try:
                os.mkdir(path2)
            except:
                pass
    new_folder=new_folder+"/"+i
def mk():    
    os.rename(new,old)
    print(os.listdir(x))
try:
    
    shutil.move(old,new_folder)
    
    print("your folder or file is now secure")
    mk()
except:
    pass


