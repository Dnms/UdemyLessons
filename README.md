# UdemyLessons

public class Ball : MonoBehaviour {


    public paddle;


	void Start () {
       

        transform.SetParent(paddle.gameObject.transform);
	}
	
	// Update is called once per frame
	void Update () {

        if (Input.GetMouseButtonDown(0))
        {
            transform.SetParent (null);

            transform.GetComponent<Rigidbody2D>().velocity = new Vector2(transform.position.x, 10f);
        }
	}
}
