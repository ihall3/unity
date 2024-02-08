# unity
unity projects

    private float speed = 5.0f;
    private float turnSpeed = 25.0f;
    private float horizontalInput;
    private float forwardInput;

        void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {

            forwardInput = Input.GetAxis("Vertical");
        horizontalInput = Input.GetAxis("Horizontal");
        // Moves car forward
        transform.Translate(Vector3.forward * Time.deltaTime * speed * forwardInput);
        // Moves car horizontal
        transform.Rotate(Vector3.up, turnSpeed * horizontalInput * Time.deltaTime);
    }
    
