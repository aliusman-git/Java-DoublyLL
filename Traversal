public class DLL1 {
    Node head;
    Node tail;
    static class Node {
        int data;
        Node prev;
        Node next;
        Node(int data) {
            this.data = data;
            this.prev = null;
            this.next = null;
        }
    }
    public void insertAtEnd(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = tail = newNode;
            return;
        }
        tail.next = newNode;
        newNode.prev = tail;
        tail = newNode;
    }
    public void printForward() {
        if (head == null) {
            System.out.println("List is empty!");
            return;
        }
        Node curr = head;
        while (curr != null) {
            System.out.print(curr.data + " <-> ");
            curr = curr.next;
        }
        System.out.println("null");
    }
    public void printBackward() {
        if (tail == null) {
            System.out.println("List is empty!");
            return;
        }
        Node curr = tail;
        while (curr != null) {
            System.out.print(curr.data + " <-> ");
            curr = curr.prev;
        }
        System.out.println("null");
    }
    public static void main(String[] args) {
        DLL1 list = new DLL1();
        list.insertAtEnd(1);
        list.insertAtEnd(5);
        list.insertAtEnd(7);
        list.insertAtEnd(9);
        System.out.println("Forward Traversal:");
        list.printForward();
        System.out.println("Backward Traversal:");
        list.printBackward();
        //My info
        System.out.println("\nName: Syed Muhammad Ali Usman\n"+"Seat number: EB25210006095\n"+"Section A");
    }
}
