# CLI Command Cheat Sheet

## Git Commands
```sh
# Undo the last commit but keep the changes
git reset --soft HEAD~1

# Undo the last commit and discard changes
git reset --hard HEAD~1

# Remove a file from Git but keep it locally
git rm --cached filename

# Amend the last commit message
git commit --amend -m "New message"

# Rename a branch locally and remotely
git branch -m oldname newname
git push origin -u newname
git push origin --delete oldname

# CLoning a git Repository
git clone https://github.com/your-username/repo.git

# Updating git repository
git add .
git commit -m "message"
git push origin main

```

## Docker Commands
```sh
# Remove all stopped containers, networks, and images
docker system prune -a

# Stop and remove all containers
docker stop $(docker ps -aq) && docker rm $(docker ps -aq)

# Remove all images
docker rmi $(docker images -q)

# Connect to a running container's shell
docker exec -it container_id bash  # Use 'sh' for Alpine-based containers

# Build and run a container
docker build -t my-image . && docker run -d --name my-container my-image

# Create a PostgreSQL container
docker run --name postgres-db -e POSTGRES_USER=user -e POSTGRES_PASSWORD=password -e POSTGRES_DB=mydb -p 5432:5432 -d postgres

# Create a Next.js app
docker run --rm -v "$PWD":/app -w /app node npx create-next-app@latest my-next-app

# Create a React app
docker run --rm -v "$PWD":/app -w /app node npx create-react-app my-react-app

# Create a Vite app
docker run --rm -v "$PWD":/app -w /app node npx create-vite@latest my-vite-app

# Create an Express app
docker run --rm -v "$PWD":/app -w /app node npx express-generator my-express-app && cd my-express-app && npm install
```

## Node.js & NPM/Yarn Commands
```sh
# Check which package depends on a specific package
npm ls package-name
yarn why package-name

# Clear npm/yarn cache
npm cache clean --force
yarn cache clean

# Update all dependencies
npm update
yarn upgrade

# Run a package binary without installing globally
npx package-name
```

## Next.js Commands
```sh
# Create a Next.js app with TypeScript
npx create-next-app@latest my-next-app --ts

# Start a Next.js development server
npm run dev

# Build for production
npm run build

# Export static files
npm run export
```

## Vite Commands
```sh
# Create a Vite project
npx create-vite@latest my-vite-app

# Start Vite development server
npm run dev

# Build for production
npm run build

# Preview the built project
npm run preview
```

## PostgreSQL Commands
```sh
# Connect to a PostgreSQL database
psql -U username -d database_name

# List all databases
\l

# List all tables in a database
\dt
```

---
This cheat sheet covers some of the most useful but often forgotten commands for web development. Happy coding! 🚀
