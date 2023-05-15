# Unity-animation-code
this repo contains code for three unique animation states in unity. 
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class animationStateController : MonoBehaviour
{
    private Vector3 MoveDirection = Vector3.zero;
    private Animator _Anim;
    private bool _isWalking = false;
    private bool _isrunning = false;
    private void Start()
}
    _anim = GetComponent<Animator>();
}

void Update()
{
    var x = Input.GetAxis("horizontal") * Time.deltaTime * 150.0f;

    transform.Rotate(0, x, 0);

    if (input.GetKey(KeyCode.LeftShift) && Input.GetKey("w"))
    {
        { if (!_isRunning)
                _isRunning = true
             _anim.Play("RUnning");
        }
        var z = Input.GetAxis("Vertical") * Time.deltaTime * 6.0f;
        transform.TRanslate(0, 0, z); // only move when "w" is pressed.
    }
    else if (Input.GetKey("w"))

    {
        if (!_iswalking && !_isRunning)
        {
            _isWalking = true
            _anim.Play("Walking");
        }
        var z = Input.GetAxis("Vertical") * Time.deltaTime * 3.0f;
        transform.Translate(0, 0, z); //only move when "w" is pressed. 
    }
    else
    {
        if (_isWalking || _isRunning)
        {
            _anim.Play("Unarmed Idle 01");
        }
        _isWalking = false;
        _isRunning = false;
        
    }
   

}
