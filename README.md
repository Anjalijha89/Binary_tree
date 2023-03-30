# Binary_tree


import java.util.*;
public class Binary_Tree {

    //1
    /*static class Node
    {
        int data;
        Node left;
        Node right;

        Node(int data)
        {
            this.data = data;
            this.left = null;
            this.right = null;
        }
    }
    static class Binarytree
    {
        static int ind = -1;
        public static Node buildtree(int nodes[])
        {
            ind++;
            if(nodes[ind] == -1)
            {
                 return null;
            }
            Node newnode = new Node(nodes[ind]);
            newnode.left = buildtree(nodes);
            newnode.right = buildtree(nodes);
            return newnode;
        }
    }
    public static void main(String args[])
    {
        int nodes[] = {1,2,4,-1,-1,5,-1,-1,3,-1,6,-1,-1};
        Binarytree  tree = new Binarytree();
       // tree.buildtree(nodes);
        Node root = tree.buildtree(nodes);
        System.out.println(root.data);
    }

     */


    //2 preorder traversal
    /*static class Node
    {
        int data;
        Node left;
        Node right;

        Node(int data)
        {
            this.data = data;
            this.left = null;
            this.right = null;
        }
    }
    static class Binarytree {
        static int ind = -1;

        public static Node buildtree(int nodes[]) {
            ind++;
            if (nodes[ind] == -1) {
                return null;
            }
            Node newnode = new Node(nodes[ind]);
            newnode.left = buildtree(nodes);
            newnode.right = buildtree(nodes);
            return newnode;
        }

        public static void preorder(Node root) {
            if (root == null) {
                return;
            }
            System.out.print(root.data + " ");
            preorder(root.left);
            preorder(root.right);
        }
    }
    public static void main(String args[])
    {
        int nodes[] = {1,2,4,-1,-1,5,-1,-1,3,-1,6,-1,-1};
        Binarytree  tree = new Binarytree();
        Node root = tree.buildtree(nodes);
        //System.out.println(root.data);
        tree.preorder(root);
    }

     */


    //3 Inorder traversal
   /* static class Node
    {
        int data;
        Node left;
        Node right;

        Node(int data)
        {
            this.data = data;
            this.left = null;
            this.right = null;
        }
    }
    static class Binarytree
    {
        static int ind = -1;
        public static Node buildtree(int nodes[])
        {
            ind++;
            if(nodes[ind] == -1)
            {
                return null;
            }
            Node newnode = new Node(nodes[ind]);
            newnode.left = buildtree(nodes);
            newnode.right = buildtree(nodes);
            return newnode;
        }
        public static void Inorder(Node root)
        {
            if(root==null)
            {
                return;
            }
            Inorder(root.left);
            System.out.print(root.data+" ");
            Inorder(root.right);
        }
    }
    public static void main(String args[])
    {
        int nodes[] = {1,2,4,-1,-1,5,-1,-1,3,-1,6,-1,-1};
        Binarytree  tree = new Binarytree();
        Node root = tree.buildtree(nodes);
        tree.Inorder(root);
    }

    */



    //4 Post order traversal
    /*static class Node
    {
        int data;
        Node left;
        Node right;

        Node(int data)
        {
            this.data = data;
            this.left = null;
            this.right = null;
        }
    }
    static class Binarytree
    {
        static int ind = -1;
        public static Node buildtree(int nodes[])
        {
            ind++;
            if(nodes[ind] == -1)
            {
                return null;
            }
            Node newnode = new Node(nodes[ind]);
            newnode.left = buildtree(nodes);
            newnode.right = buildtree(nodes);
            return newnode;
        }
        public static void Postorder(Node root)
        {
            if(root==null)
            {
                return;
            }
            Postorder(root.left);
            Postorder(root.right);
            System.out.print(root.data+" ");

        }
    }
    public static void main(String args[])
    {
        int nodes[] = {1,2,4,-1,-1,5,-1,-1,3,-1,6,-1,-1};
        Binarytree  tree = new Binarytree();
        Node root = tree.buildtree(nodes);
        tree.Postorder(root);
    }

     */



    //5. Level order Traversal
    /*static class Node
    {
        int data;
        Node left;
        Node right;

        Node(int data)
        {
            this.data = data;
            this.left = null;
            this.right = null;
        }
    }
    static class Binarytree
    {
        static int ind = -1;
        public static Node buildtree(int nodes[])
        {
            ind++;
            if(nodes[ind] == -1)
            {
                return null;
            }
            Node newnode = new Node(nodes[ind]);
            newnode.left = buildtree(nodes);
            newnode.right = buildtree(nodes);
            return newnode;
        }
        public static void Levelorder(Node root)
        {
            if(root==null)
            {
                return;
            }
            Queue<Node> q = new LinkedList<>();
            q.add(root);
            q.add(null);
            while(!q.isEmpty())
            {
                Node currNode = q.remove();
                if(currNode == null)
                {
                    System.out.println();
                    if(q.isEmpty())
                    {
                        break;
                    }
                    else
                    {
                        q.add(null);
                    }
                }
                else
                {
                    System.out.print(currNode.data+" ");
                    if(currNode.left != null)
                    {
                        q.add(currNode.left);
                    }
                    if(currNode.right != null)
                    {
                        q.add(currNode.right);
                    }
                }
            }


        }
    }
    public static void main(String args[])
    {
        int nodes[] = {1,2,4,-1,-1,5,-1,-1,3,-1,6,-1,-1};
        Binarytree  tree = new Binarytree();
        Node root = tree.buildtree(nodes);
        tree.Levelorder(root);
    }

     */




    //6 Height of tree
   /* static class Node {
        int data;
        Node left;
        Node right;

        Node(int data) {
            this.data = data;
            this.left = null;
            this.right = null;
        }
    }
        public static int height(Node root)
        {
            if(root == null)
            {
                return 0;
            }
            int lh = height(root.left);
            int rh = height(root.right);
            return Math.max(lh,rh)+1;
        }
    public static void main(String args[])
    {
        Node root = new Node(1);
        root.left = new Node(2);
        root.right = new Node(3);
        root.left.left = new Node(4);
        root.left.right = new Node(5);
        root.right.left = new Node(6);
        root.right.right = new Node(7);
        System.out.println(height(root));


    }

    */



    //7 Count nodes of a tree
    /*static class Node {
        int data;
        Node left;
        Node right;

        Node(int data) {
            this.data = data;
            this.left = null;
            this.right = null;
        }
    }
    public static int count(Node root)
    {
        if(root == null)
        {
            return 0;
        }
        int leftcount = count(root.left);
        int rightcount = count(root.right);
        return leftcount+rightcount+1;

    }
    public static void main(String args[])
    {
        Node root = new Node(1);
        root.left = new Node(2);
        root.right = new Node(3);
        root.left.left = new Node(4);
        root.left.right = new Node(5);
        root.right.left = new Node(6);
        root.right.right = new Node(7);
        System.out.println(count(root));
         }

     */




    //8 Sum of nodes
    static class Node {
        int data;
        Node left;
        Node right;

        Node(int data) {
            this.data = data;
            this.left = null;
            this.right = null;
        }
    }
    public static int sum(Node root)
    {
        if(root == null)
        {
            return 0;
        }
        int leftcount = sum(root.left);
        int rightcount = sum(root.right);
        return leftcount+rightcount+root.data;

    }
    public static void main(String args[])
    {
        Node root = new Node(1);
        root.left = new Node(2);
        root.right = new Node(3);
        root.left.left = new Node(4);
        root.left.right = new Node(5);
        root.right.left = new Node(6);
        root.right.right = new Node(7);
        System.out.println(sum(root));


    }


}
