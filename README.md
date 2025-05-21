using UnityEngine;  

public class PlayerMovement : MonoBehaviour {  
    public FixedJoystick joystick;  
    public float moveSpeed = 8f;  
    private CharacterController controller;  

    void Start() => controller = GetComponent<CharacterController>();  

    void Update() {  
        Vector3 direction = new Vector3(joystick.Horizontal, 0, joystick.Vertical);  
        controller.Move(direction * moveSpeed * Time.deltaTime);  
    }  
}# Game