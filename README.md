Instructions
1. Create Your Workspace Directory
First, create a directory where both repositories will live:
mkdir your-workspace
cd your-workspace
2. Clone the Original Node.js Repository
Clone the main application repository first:

git clone https://github.com/Norbert305/crud-react-node-mySQL-go

3. Clone the Containerization Repository
Next, clone this repository which contains the Docker configuration. It needs to be at the same level as the first repository:

git clone https://github.com/p-archamb/ContainerizeItAssignment

4. Start the Application
Navigate to the containerization repository and start the Docker containers:

cd containerizeitassignment

docker compose up