# CG-L1
Creating the first window program displaying a plane figure (triangle)

  glutDisplayFunc(RenderSceneCB)
  function sets the display callback for the current window, taking callback function needed for rendering as an argument
  
	glClear(GL_COLOR_BUFFER_BIT)
  function clears buffers to preset values, argument indicates the buffers currently enabled for color writing

	glEnableVertexAttribArray(0)
  function enables or disables a generic vertex attribute array depending on the argument
  
	glBindBuffer(GL_ARRAY_BUFFER, VBO)
  function specifies the target to which the buffer object is bound, argument is interpreted as an offset within the buffer object
  
	glVertexAttribPointer(0, 3, GL_FLOAT, GL_FALSE, 0, 0)
  function defines an array of generic vertex attribute data with: 
  the index of the generic vertex attribute to be modified, 
  the number of components per generic vertex attribute,
  the data type of each component in the array,
  the value showing that fixed-point data values should be converted directly as fixed-point values,
  the byte offset between consecutive generic vertex attributes,
  a offset of the first component of the first generic vertex attribute in the array in the data store of the buffer
  
	glDrawArrays(GL_TRIANGLES, 0, 3)
  function renders primitives from array data, with arguments defining 
  what kind of primitives to render, 
  the starting index in the enabled arrays and 
  the number of indices to be rendered
  
	glutSwapBuffers()
  swaps roles of the front- and backbuffers on the layer in use for the current window

	glutInit(&argc, argv)
  initializes the GLUT library
  
	glutInitDisplayMode(GLUT_DOUBLE | GLUT_RGBA)
  sets the initial display mode, argument defines the RGBA mode (RGB + alpha)
  
	glutInitWindowSize(1024, 768);
	glutInitWindowPosition(100, 100)
  set the initial window size and position respectively
  
	glutCreateWindow("Tutorial")
  creates a top-level window, the window system will label the window with the argument name
  
	glClearColor(0.0f, 0.0f, 1.0f, 0.0f)
  specifies clear values for the color buffers, with red, green, blue colors and alpha value used when the color buffers are cleared

	glGenBuffers(3, &VBO)
  generates buffer object names, the first argument is the number of buffer object names to be generated, the second one is an array in which the names are stored
  
	glBufferData(GL_ARRAY_BUFFER, sizeof(Vertices), Vertices, GL_STATIC_DRAW)
  creates a buffer object's data store
  
  glutDisplayFunc(RenderSceneCB) sets the display callback for the current window
  
	glutMainLoop()
  passes control to GLUT which begins its internal loop
  
  We have learnt to create simple programs using tools specific for this application programming interface.
