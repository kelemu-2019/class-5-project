# class-5-project

## CICD

CICD is set up with CircleCI which uses docker containers to execute each step. The steps for the frontend are the equivalent of

```
docker run --rm --workdir /app -v (pwd)/frontend:/app --name tmp node yarn install
docker run --rm --workdir /app -v (pwd)/frontend:/app --name tmp node yarn test
docker run --rm --workdir /app -v (pwd)/frontend:/app --name tmp node yarn build
```

What this does is, it executes the three yarn (equivalent to npm) steps in an isolated container environment. What are containers? In short, the future of computing. It's not an overstatement, they are and will be everywhere. Google literally runs *everything* in containers. 

There are processes predefined for the following two configurations:

1. a frontend based on 

## Linting

The frontend (and hopefully also soon the backend) should be linted. Use [this article](https://medium.com/@pppped/extend-create-react-app-with-airbnbs-eslint-config-prettier-flow-and-react-testing-library-96627e9a9672) for guidance