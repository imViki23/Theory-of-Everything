# Data structures

## Linked List

**References**

- https://www.youtube.com/watch?v=njTh_OwMljA&list=PLLXdhg_r2hKA7DPDsunoDZ-Z769jWn4R8&index=3&t=1s

**Implementation**

```js
class Node {
    data;
    next = null; // Node

    constructor(data) {
        this.data = data;
    }
}

class LinkedList {
    head = null;
    size = 0;

    add(data) {
        if (this.head === null) {
            this.head = new Node(data);
            this.size++;
            return;
        }
        let current = this.head;
        while (current.next !== null) {
            current = current.next;
        }
        current.next = new Node(data);
        this.size++;
    }

    delete(index) {
        if (this.head === null) {
            throw new Error('List is empty')
        }
        if (index < 0) {
            throw new Error('Index cannot be negative value')
        }
        if (index > this.size - 1) {
            throw new Error('Index exceed list size')
        }
        
        // Deleting head node
        if (index === 0) {
            this.head = this.head.next;
            this.size--;
            return;
        }

        let counter = 0;
        let prev = null;
        let current = this.head;

        while (counter < index) {
            prev = current;
            current = current.next;
            counter++;
        }

        prev.next = current.next;
        this.size--;
    }

    toString() {
        let str = "[";
        if (this.head != null) {
            let current = this.head;
            str += current.data;
            while (current.next != null) {
                current = current.next;
                str += `, ${current.data}`;
            }
        }
        str += "]";
        return str;
    }
}
```