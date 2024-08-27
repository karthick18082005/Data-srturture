#include <stdio.h>
#include <stdlib.h>
struct Node {
    int data;
    struct Node *left;
    struct Node *right;
};
struct Node* createNode(int data) {
    struct Node* newNode =
      (struct Node*)malloc(sizeof(struct Node));
    newNode->data = data;
    newNode->left = NULL;
    newNode->right = NULL;
    return newNode;
}
int main() {
    // Initialize and allocate memory for tree nodes
    struct Node* firstNode = createNode(2);
    struct Node* secondNode = createNode(3);
    struct Node* thirdNode = createNode(4);
    struct Node* fourthNode = createNode(5);
    firstNode->left = secondNode;
    firstNode->right = thirdNode;
    secondNode->left = fourthNode;
    return 0;
}
