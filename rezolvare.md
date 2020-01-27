public class Main {

    public static void main(String args[]) throws Exception {
        int[] floors = new int[]{1, 0, 5, 4, 1, 7, 3, 2, 6, 0, 1};
        int liftA = 0;
        int liftB = 7;
  

        for (int requestedFloor: floors) {
             int distanceLiftA = Math.abs(requestedFloor - liftA);
             int distanceLiftB = Math.abs(requestedFloor - liftB);

            if (distanceLiftA < distanceLiftB) {
                if(requestedFloor < liftA)
                    System.out.println("Elevator A goes down at floor " + requestedFloor + ".");
                else if(requestedFloor > liftA)
                    System.out.println("Elevator A goes up at floor " + requestedFloor + ".");
                liftA = requestedFloor;
            }
            else if (distanceLiftA == distanceLiftB) {
                if (liftA < liftB) {
                    if(requestedFloor < liftA)
                        System.out.println("Elevator A goes down at floor "+ requestedFloor + "." );
                    else if(requestedFloor > liftA)
                        System.out.println("Elevator A goes up at floor "+ requestedFloor + "." );
                    liftA = requestedFloor;
                    
                } else {
                     if(requestedFloor < liftB)
                        System.out.println("Elevator B goes down at floor "+ requestedFloor + "." );
                    else if(requestedFloor > liftB)
                        System.out.println("Elevator B goes up at floor "+ requestedFloor + "." );
                    liftB = requestedFloor;
                    
                }
            } else {
                if(requestedFloor < liftB)
                        System.out.println("Elevator B goes down at floor "+ requestedFloor + "." );
                    else if(requestedFloor > liftB)
                        System.out.println("Elevator B goes up at floor "+ requestedFloor + "." );
                    liftB = requestedFloor;
            }
        }
    }
}
