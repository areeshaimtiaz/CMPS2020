#include <iostream>
#include <string>
using namespace std;

// Node structure for the linked list
struct Node
{
    string data;
    Node * next;
};

// Function to create a new node
Node * createNode(const string & value)
{
    Node * newnode = new Node;
    newnode->data = value;
    newnode->next = NULL;
    return newnode;
}

// Function to add a node at the front of the linked list
void addToFront(Node * & head, const string & value)
{
    Node * newnode = createNode(value);
    newnode->next = head;
    head = newnode;
}

// Function to find a node in the linked list and move it to the front
void moveToFront(Node *& head, const string & value)
{
    if ((head == NULL) || (head->data == value))
    {
        return; // No need to move if the node is already at the front or the list is empty
    }

    Node * prev = NULL;
    Node * current = head;

    while ((current != NULL) && (current->data != value))
    {
        prev = current;
        current = current->next;
    }

    if (current == NULL)
    {
        return; // Node not found in the list
    }

    prev->next = current->next;
    current->next = head;
    head = current;
}

// Function to display the linked list
void displayList(const Node * head)
{
    const Node * current = head;

    while (current != NULL)
    {
        cout << current->data << endl;
        current = current->next;
    }
}

int main()
{
    Node * head = NULL;
    string input;

    while (true)
    {
        cout << "Enter a string (or 'quit' to exit): ";
        getline(cin, input);

        if (input == "quit")
        {
            break;
        }

        // Check if the string is already in the list and move it to the front
        moveToFront(head, input);

        // If the string is not in the list, add it to the front
        if ((head == NULL) || (head->data != input))
        {
            addToFront(head, input);
        }

        // Display the updated list
        cout << endl << "List: " << endl;
        displayList(head);
        cout << endl;
    }
    return 0;
}
                                                                                                                                            100,1         Bo
