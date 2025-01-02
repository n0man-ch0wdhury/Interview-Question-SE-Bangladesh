# Custom Serializer

[Watch the video](https://www.tella.tv/video/custom-serializer-1-6vyk)

### Input

![Input Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/c1fc3c43-0252-4be7-9e4f-e8813d7cf35b/31559cf9-0d4a-4000-9118-7678305d94ae/image.png)

### Output

![Output Image](https://prod-files-secure.s3.us-west-2.amazonaws.com/c1fc3c43-0252-4be7-9e4f-e8813d7cf35b/c0b8dcb1-8a34-46d3-915c-4595f64cb9f0/image.png)

<aside>
💡 This challenge was solved by one of our engineers internally.

1. It took ~20 minutes. 
2. Our final file (including input data) is 59 lines long.

</aside>

# Environment

1. You definitely need NodeJS version 20 such that you can run .mjs files directly.

# What To Build

1. We have to build a custom serializer for weird data. We call it weird cause it can be an array, object, string or number.
2. We have to serialize it and make a string out of it. The rules are as follows: 
    - **Number Serialization**
        - Prefix number values with "num:"
    - **String Serialization**
        - Prefix string values with "str:"
        - Apply a special transformation for strings having > 2 characters
        - **Transformation:** First character + (length - 2) + Last character
    - **Array Serialization**
        - Prefix array values with "arr:"
        - Serialize each array element
        - Concatenate serialized elements without separators
    - **Object Serialization**
        - Prefix object values with "obj:"
        - Serialize only object values by their keys
        - Concatenate serialized values without separators
        - Ignore key names in final output
    - **Error Handling**
        - Prefix object values with "err:"
        - Value will be “unknown”.
        - Example: Return "err:unknown" for unrecognized data types

# Details

1. Don’t use any external libraries.

# Let’s Start

1. **Clone the repo first:**

    `git clone git@github.com:fringecore/fringecore-backend-challenge-custom-serializer.git`  

2. **Nevigate to Directory:**

    `cd fringecore-backend-challenge-custom-serializer`

3. **Open your favorite code editor (like VSCode for example):**

    `code .`

4. **Test run our code:**

    `node ./challenge.mjs`

HAPPY CODING! 🎉

# Partial

Just know that we fully understand that these challenges are actually pretty tough. Hence it is surely not an all-or-nothing evaluation scheme. If you hit any of the features below you’re doing great. Every time you achieve one of these points, pat yourself on the back.

1. You have started the challenge.
2. Your custom serializer is working only for primitive data types (i.e., string or number).
3. Your custom serializer is partially complete.

# Submission

1. First add the fringecore remote repository:
    
    `git remote add fringecore ssh://submission.fringecore.sh/<applicant_id>/fringecore-backend-challenge-custom-serializer`
        > **Note:** Your application_id is case sensitive.
    
2. Then just push into it:
    
    `git push fringecore main`
    
You may see a warning like "The authenticity of host '[submission.fringecore.sh](http://submission.fringecore.sh/) (xx.xx.xx.xx)' can't be established," just type yes and press enter to continue.
