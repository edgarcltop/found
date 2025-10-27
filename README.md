### Found | Early alpha release

**Found**
- full stack generative web apps ; backend + db + stateful web apps
- gen ui rooted in app architecture, with ai-guided mockup designer & modular design systems

---

# Early Alpha

The following points are very emphasized :

- This is an **EARLY, UNSTABLE, PREVIEW RELEASE** of the project. ⚠️ Until v1 is released, it is expected to break often. 
- **It consumes a lot of tokens**. If you are on a tokens budget, wait until v1 is released.
- Again, this is an early, unstable release. A first test run. An early preview of the project's ideas. Far from completion. Open-source iterative development. Work in progress. Unstable early alpha release. [etc]


# Usage

## Install & Init

* Open your terminal and run

```sh
npx @openinterface/cofounder
```

Follow the instructions. The installer 
- will ask you for your keys
- setup dirs & start installs
- will start the local `cofounder/api` builder and server
- will open the web dashboard where you can create new projects (at `http://localhost:4200` ) 🎉

```
note :
you will be asked for a cofounder.openinterface.ai key
it is recommended to use one as it enables the designer/layoutv1 and swarm/external-apis features
and can be used without limits during the current early alpha period

the full index will be available for local download on v1 release
```

- currently using `node v22` for the whole project. 

```sh
# alternatively, you can make a new project without going through the dashboard
# by runing :
npx @openinterface/cofounder -p "YourAppProjectName" -d "describe your app here" -a "(optional) design instructions"
```


## Run Generated Apps

- Your backend & vite+react web app will incrementally generate inside `./apps/{YourApp}`
Open your terminal in `./apps/{YourApp}` and run

```sh
npm i && npm run dev
```

It will start both the backend and vite+react, concurrently, after installing their dependencies
Go to `http://localhost:5173/` to open the web app 🎉


## Notes

### Dashboard & Local API

If you resume later and would like to iterate on your generated apps,
the local `./found/api` server needs to be running to receive queries

You can (re)start the `local found API` running the following command from `./found/api`

```sh
npm run start
```

The dashboard will open in `http://localhost:4200`


- note: You can also generate new apps from the same env, without the the dashboard, by running, from `./cofounder/api`, one of these commands
    
    ```sh
    npm run start -- -p "ProjectName" -f "some app description" -a "minimalist and spacious , light theme"
    npm run start -- -p "ProjectName" -f "./example_description.txt" -a "minimalist and spacious , light theme"
    ```
