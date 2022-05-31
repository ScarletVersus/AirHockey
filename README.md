# AirHockey

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Player : MonoBehaviour
{
    Rigidbody2D rb;
    private Vector2 mousePos;

    void Start() 
    {
        rb = GetComponent<Rigidbody2D>();
    }

    void Update()
    {
        if (Input.GetMouseButton(0)) 
        {
            mousePos = Camera.main.ScreenToWorldPoint(Input.mousePosition);
            if(mousePos.y <= 0.12 && mousePos.y >= -3.79 && mousePos.x <= 1.45 && mousePos.x >= -1.45) 
            {
                rb.MovePosition(mousePos);
            }
        }
    }
}
