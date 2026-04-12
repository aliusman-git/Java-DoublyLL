public class Dll {
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
    //insert at front
    public void insertAtFront(int data) {
        Node newNode = new Node(data);
        if (head == null) {
            head = tail = newNode;
            return;
        }
        newNode.next = head;
        head.prev = newNode;
        head = newNode;
    }
    //insert at end
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
    //insert at specific position
    public void insertAtPosition(int data, int position) {
        Node newNode = new Node(data);
        if (position == 1) {
            insertAtFront(data);
            return;
        }
        Node current = head;
        int count = 1;
        while (count < position - 1 && current != null) {
            current = current.next;
            count++;
        }
        if (current == null || current.next == null) {
            insertAtEnd(data);
            return;
        }
        newNode.next = current.next;
        newNode.prev = current;
        current.next.prev = newNode;
        current.next = newNode;
    }
    //delete at front
    public void deleteAtFront() {
        if (head == null) {
            System.out.println("List is empty!");
            return;
        }
        if (head == tail) {
            head = tail = null;
            return;
        }
        head = head.next;
        head.prev = null;
    }
    //delete at end
    public void deleteAtEnd() {
        if (head == null) {
            System.out.println("List is empty!");
            return;
        }
        if (head == tail) {
            head = tail = null;
            return;
        }
        tail = tail.prev;
        tail.next = null;
    }
        //delete at specific position
    public void deleteAtPosition(int position) {
        if (head == null) {
            System.out.println("List is empty!");
            return;
        }
        if (position == 1) {
            deleteAtFront();
            return;
        }
        Node current = head;
        int count = 1;
        while (count < position && current != null) {
            current = current.next;
            count++;
        }
        if (current == null) {
            System.out.println("Position out of range!");
            return;
        }
        if (current == tail) {
            deleteAtEnd();
            return;
        }
        current.prev.next = current.next;
        current.next.prev = current.prev;
    }
        //delete by value
    public void deleteByValue(int key) {
        if (head == null) {
            System.out.println("List is empty!");
            return;
        }
        if (head.data == key) {
            deleteAtFront();
            return;
        }
        if (tail.data == key) {
            deleteAtEnd();
            return;
        }
        Node current = head;
        while (current != null) {
            if (current.data == key) {
                current.prev.next = current.next;
                current.next.prev = current.prev;
                return;
            }
            current = current.next;
        }
        System.out.println(key + " not found!");
    }
        //searching value
    public void search(int key) {
        if (head == null) {
            System.out.println("List is empty!");
            return;
        }
        Node current = head;
        int position = 1;
        while (current != null) {
            if (current.data == key) {
                System.out.println("Found " + key + " at position " + position);
                return;
            }
            current = current.next;
            position++;
        }
        System.out.println(key + " not found!");
    }
        //printing the length
    public int length() {
        int count = 0;
        Node current = head;
        while (current != null) {
            count++;
            current = current.next;
        }
        return count;
    }
        //print the list
    public void printlist() {
        if (head == null) {
            System.out.println("List is empty ");
            return;
        }
        Node curr = head;
        while (curr != null) {
            System.out.print(curr.data + " <-> ");
            curr = curr.next;
        }
        System.out.println("null");
    }
        public void deleteEntireList() {
        head = null;
        tail = null;
    }

    public static void main(String[] args) {
        Dll list = new Dll();

        list.insertAtEnd(1);
        list.insertAtEnd(5);
        list.insertAtEnd(9);
        list.insertAtFront(0);
        System.out.println("\toriginal list");
        list.printlist();
        System.out.println("\tinserting at specific position");
        list.insertAtPosition(3, 2);
        list.printlist();
        System.out.println("Length: " + list.length());
        System.out.println("\tsearching element");
        list.search(9);
        list.search(99);
        list.printlist();
        System.out.println("\tdelete at front");
        list.deleteAtFront();
        list.printlist();
        System.out.println("\tdelete at end");
        list.deleteAtEnd();
        list.printlist();
        System.out.println("\tdelete at position");
        list.deleteAtPosition(2);
        list.printlist();
        System.out.println("\tdelete by value");
        list.deleteByValue(5);
        list.printlist();
        System.out.println("\tdelete entire list");
        list.deleteEntireList();
        list.printlist();
        //My info
        System.out.println("\nName: Syed Muhammad Ali Usman\n"+"Seat number: EB25210006095\n"+"Section A");
    }
}
