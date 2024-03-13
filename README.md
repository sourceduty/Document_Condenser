![Document Condenser](https://github.com/sourceduty/Document_Condenser/assets/123030236/9de6a62d-cd68-4305-89cd-919ca416fded)

### Document Condenser Concept

Condense text documents by removing blank spaces and paragraph spaces. Reduce the overall file size by saving the condensed text into a plain text file. Included in the plain text file is a pseudocode to remember the structure of the text in the original document. 

<details><summary>Example Document Structure Pseudocode</summary>

 ```
1. Define a Node structure
    - Content: Text contained in the node
    - Type: Type of the node (e.g., Heading, Paragraph, List)
    - Children: A list of child nodes

2. Create a function to process the document
    Function ProcessDocument(document)
        Initialize an empty list DocumentStructure to hold the top-level nodes
        For each element in the document
            Node = ProcessElement(element)
            Add Node to DocumentStructure
        End For
        Return DocumentStructure
    End Function

3. Create a function to process each element based on its type
    Function ProcessElement(element)
        Create a new Node
        Set Node.Content to the text content of the element
        Set Node.Type based on the element type (e.g., heading, paragraph)
        If the element can contain child elements (like a section or a list)
            For each child element in the element
                ChildNode = ProcessElement(child)
                Add ChildNode to Node.Children
            End For
        End If
        Return Node
    End Function

4. To display or use the structure, traverse the DocumentStructure
    Function TraverseStructure(nodes, depth = 0)
        For each node in nodes
            Print indentation based on depth and node content (and type if necessary)
            If node has children
                TraverseStructure(node.Children, depth + 1)
            End If
        End For
    End Function
 ```

</details>

This pseudocode outlines the basic idea of processing a document to remember its structure. The ProcessDocument function starts the process by going through each top-level element in the document, processing each one with ProcessElement, which is recursive for elements that can contain other elements. The structure is then stored in a nested way, reflecting the document's hierarchy. The TraverseStructure function is an example of how you might use the stored structure to display it or perform other operations.

***

Copyright (C) 2024, Sourceduty - All Rights Reserved.
