# Java_EE_Udemy39
Cascading and Propagation of persist and remove actions

Inside Flight:

    @OneToOne( cascade = { CascadeType.PERSIST, CascadeType.REMOVE })
	  @JoinColumn(name= "airplane_fk")
	  private Airplane airplaneDetail;
    
This now enables the Flight list to update automatically. This also means that if a Pilot is added to a flight and the flight is deleted
the Pilot will also now be deleted.
