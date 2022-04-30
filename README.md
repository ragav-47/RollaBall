# Roll a Ball

## Aim:
To Roll a Ball using C# program in unity .

## Algorithm:
### Step 1:
Create New Scene on unity game engine.
### Step 2:
Right click on Hierarchy create 3D Object.
### Step 3:
Click Hierarchy -> 3DObject -> Sphere Hierarchy -> 3DObject -> plane Hierarchy.
### Step 4:
Create a folder in project and name as Materials Material folder -> Create -> Material (Name: Sphere) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Drag the Cylinder to the plane and release the mouse

Create a folder in project and name as Materials Material folder -> Create -> Material (Name: Plane) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Drag the Capsule to the plane and release the mouse
### Step 5:
Create a folder name Coding and create a C# file to add the coding in it.
### Step 6:
To add our C# Script file to our selected object, click on the C# Script file and drag it to Sphere objects in the Hierarchy window and run the application.
### Step 7:
After run the application, you press the WASD and space key the ball will move and jump.

## Program:
```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Object1 : MonoBehaviour
{
    // Start is called before the first frame update
    public float xmove = 7.0f;
    public float zmove = 5.0f;
    public float ymove = 150.0f;
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f;
        if(Input.GetKey(KeyCode.UpArrow))
        {
            x += xmove;
        }
        if(Input.GetKey(KeyCode.DownArrow))
        {
            x -= xmove;
        }
        float z = 0.0f;
        if(Input.GetKey(KeyCode.RightArrow))
        {
            z -= zmove;
        }
        if(Input.GetKey(KeyCode.LeftArrow))
        {
            z += zmove;
        }
        float y = 0.0f;
        if(Input.GetKeyDown(KeyCode.Space))
        {
            y = ymove;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);
    }
}
```

## Output:

![Screenshot (50)](https://user-images.githubusercontent.com/75235488/166115092-da754059-5843-471f-8484-5fea5ce6ff07.png)

https://user-images.githubusercontent.com/75235488/166115238-fdcbe2ee-05cf-48e0-ac94-828dac6d1afb.mp4



## Result:
Thus, The 3D application for Roll the Ball objects in unity is developed successfully.
