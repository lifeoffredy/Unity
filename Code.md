using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class newTeleport : MonoBehaviour
{
    public Vector3 targetPosition; // The position where you want the sphere to move

    // Start is called before the first frame update
    void Start()
    {
        targetPosition = new Vector3(-19050.11f, 1710f, -21775.97f);
    }

    // Update is called once per frame
    void Update()
    {

    }

    // Upon collision with another GameObject, another GameObject will turn green
    private void OnTriggerEnter(Collider other)
    {
        // Use the Console to understand what your code is doing
        Debug.Log("HIT DETECTED!");

        // Move the ball to the new location!
        GameObject.FindWithTag("ball").transform.position = targetPosition;
        GameObject.FindWithTag("ball1").transform.position = targetPosition;
        GameObject.FindWithTag("ball2").transform.position = targetPosition;
        GameObject.FindWithTag("ball3").transform.position = targetPosition;
        GameObject.FindWithTag("ball4").transform.position = targetPosition;

        // Reset the velocity to zero once the ball arrives at the new location
        // Rigidbody ballRigidbody = GameObject.FindWithTag("ball").GetComponent<Rigidbody>();
        // ballRigidbody.velocity = Vector3.zero;
    }
}
