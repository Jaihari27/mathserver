# Ex.05 Design a Website for Server Side Processing
# Date:
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
url.py rom django.contrib import admin from django.urls import path from bmiapp import views
urlpatterns = [ path('admin/', admin.site.urls), path('', views.calculate_bmi, name='calculate_bmi'), ]
views.py from django.shortcuts import render
def calculate_bmi(request): bmi = None # Default value
```if request.method == "POST":
    height = float(request.POST.get("height"))
    weight = float(request.POST.get("weight"))
    bmi = weight / (height * height)

    # Print to server console for debugging
    print("Height:", height)
    print("Weight:", weight)
    print("BMI calculated:", bmi)

return render(request, "bmiapp/template.html", {"BMI": bmi})
```
web.html
<title>BMI Calculator</title>
# SERVER SIDE PROCESSING:
<img width="1022" height="526" alt="image" src="https://github.com/user-attachments/assets/f90c11ca-474d-4726-80ae-36ecb42fcf54" />

# HOMEPAGE:
<img width="1029" height="529" alt="image" src="https://github.com/user-attachments/assets/523e1ba6-0266-4082-a505-c1ca91423a19" />

# RESULT:
The program for performing server side processing is completed successfully.
