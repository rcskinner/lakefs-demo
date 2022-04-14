# LakeFS Demo 

Script / Internal planning document for plannign the sales pitch

What is LakeFS? 
LakeFS is an version control for object storage that provides Git like operations on object storage


LakeFS  
https://docs.lakefs.io/assets/img/wrapper.png
https://lakefs.io/data-lakes/


## 3 Main Value Streams: 

    Development
        - Experiment: Create safe experiment space for development teams 
        - Test: Test hypothesies on production environment without risking production data
        - Collaborate: Collaborate with engineering teams to develop data engineering workflows

    Deployment
        - Merges and Hooks: 
        - Version Control:

    Production 
        - Rollback
        - Troubleshoot



## Demo outline: 
    
    Presentation: (10 mins)
        
        Purpose: Level set what a data lake is, why business need clean and functional data lakes,  what LakeFS does, why does that enable/drive value for the business. 

        Topics:
            - DataLakes / Why Implement Data Lakes 
            - Data Lake Challenges
            - LakeFS Overview 
            - LakeFS Value Proposition 
    
    **Technical Demo: (40 mins)**
        - LakeFS in Development (15 mins)
            - Experiment
            - Test 
            - Collaborate
        - LakeFS in Deployment (15 mins)
        - LakeFS in Production (10 mins)

    End Questions (10 mins)

    Total Time: 50 mins

Github Layout: 

    /development
        lakefs-devel.ipynb
    /deployment
        lakefs-deploy.ipynb
    /production
        lakefs-prod.ipynb



`Lakectl` Commands  
    
    <repository uri>: lakefs://demo-repo 
    <storage namespace>: s3://treeverse-demo-lakefs-storage-production/user_datapted-husky




    # Create a new repo
    lakectl repo create lakefs://demo-repo s3://treeverse-demo-lakefs-storage-production/user_adapted-husky

    # Delete an existing repository 
    lakectl repo delete lakefs://demo-repo

    # Create a new branch on a repository 
    lakectl branch create lakefs://demo-repo/feature -s lakefs://demo-repo/main