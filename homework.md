# AWS EC2 Project

### Testing the booking project locally
![image](https://github.com/V1rushB/test-repo/assets/137794637/e09bb96e-aa69-488d-be5c-032a15702ae0)

![image](https://github.com/V1rushB/test-repo/assets/137794637/2003118f-98b3-4288-8b26-c0b5cea28f83)

## preparing to push the project on GitHub

### Building the JS version of the code
![HW3](https://github.com/V1rushB/test-repo/assets/137794637/c6213d24-fe66-4dd2-a528-915c14a580a6)
  in this step we're just building the project using the `tsc` command, the JS project version will be built into './dist' directory

### Packaging the necessary files for the release on GitHub
![HW6](https://github.com/V1rushB/test-repo/assets/137794637/6dd5c9fd-a4e0-46bd-9b7a-5d5142f6a48d)
  in this step we're just packaging package.json, package-lock.json and `./dist/*` to enroll them within the release on GitHub which we'll use later on.
## Create a release on GitHub
![HW4](https://github.com/V1rushB/test-repo/assets/137794637/31fb1ad5-8713-4bc6-8fd7-5b7433285327)
  We make a tag for the release on the last commit made on the project
![HW5](https://github.com/V1rushB/test-repo/assets/137794637/9e5bb7d0-aa4c-460d-a2e6-c5bb00d1e058)

## Preparing the environment
Now we need to prepare the servers that we're gonna need to run our project.
### Setting Auto scaling groups
![HW7](https://github.com/V1rushB/test-repo/assets/137794637/c26bb40e-b1b9-416a-9ed1-df6dc969ddf5)
![hw8](https://github.com/V1rushB/test-repo/assets/137794637/91e44e71-43ac-472d-90fd-064b324b6b1a)
We choose an appropriate name
![HW9](https://github.com/V1rushB/test-repo/assets/137794637/9cc49baa-f6b7-4176-8026-367c19e92681)

### Making the template
we're gonna need our servers to start with a particular template, or more like a set of commands that will serve our needs for our project to run properly
![HW10](https://github.com/V1rushB/test-repo/assets/137794637/e29ea115-6b1e-4119-a770-a5176cd1e2dc)
  here we'll just make up a good name and a description for our template.
![HW11](https://github.com/V1rushB/test-repo/assets/137794637/87a26df4-4f46-4ea9-96c0-f3361153a565)
choosing Ubuntu as our server's running operating system and setting up the proccessor
![HW12](https://github.com/V1rushB/test-repo/assets/137794637/e90ffc4d-f8d3-48c3-bad8-97612b459921)
![HW13](https://github.com/V1rushB/test-repo/assets/137794637/dee23c1b-84d8-42d2-aa97-588b496973b6)
Notice that we need a keypair in case we run into an error we'll start debugging it from our local device.
![HW14](https://github.com/V1rushB/test-repo/assets/137794637/a380d9a8-6cad-435e-be72-4f3d74671c36)
![HW15](https://github.com/V1rushB/test-repo/assets/137794637/a1fad8f0-392c-42b0-8254-0826d165a2ba)

here we're just setting the security group.
![HW16](https://github.com/V1rushB/test-repo/assets/137794637/d4b930a1-f52a-42d6-9a0d-30a1a634418c)
![HW17](https://github.com/V1rushB/test-repo/assets/137794637/8a301e38-6422-48e2-a05b-d6b644eff964)
![hw18](https://github.com/V1rushB/test-repo/assets/137794637/4cb12c66-a2ec-4991-8ffb-e73eb11dd36f)

and here we'll need to put our template
![image](https://github.com/V1rushB/test-repo/assets/137794637/b8905f73-5bb3-449b-8967-871dbb096002)
Now our launch template has been successfully created
![hw20](https://github.com/V1rushB/test-repo/assets/137794637/c3ce3f3d-0477-4824-bc58-0c45ad0b81c9)
We continue with setting up the auto scaling group
![HW21](https://github.com/V1rushB/test-repo/assets/137794637/7989db95-c854-4e09-b9a0-ffc53e6114ed)
![HW22](https://github.com/V1rushB/test-repo/assets/137794637/6d3475c7-3988-4eb3-9f26-c7b967c95b62)
![HW23](https://github.com/V1rushB/test-repo/assets/137794637/f16754d2-4f54-484a-906e-8093c802a633)
![HW24](https://github.com/V1rushB/test-repo/assets/137794637/35488123-764a-4713-b844-b98370a0be49)
![HW26](https://github.com/V1rushB/test-repo/assets/137794637/b4b0af82-398c-4304-8a01-4f81d4f63772)
![HW27](https://github.com/V1rushB/test-repo/assets/137794637/6f921002-e8b5-42a0-9c1c-34713aef9b39)
We're allowing health checks and set the path to `/health` (as our project suggests) because we'll need them later on to confirm that our server is runnning just fine. 
![HW28](https://github.com/V1rushB/test-repo/assets/137794637/0e9f4091-fc7e-4c7a-b089-fd16b1430926)
setting up the group size which will manipulate the number of servers running at some moment, minimum, maximum and the desired size to suit our needs.
![HW29](https://github.com/V1rushB/test-repo/assets/137794637/1a963b57-e858-46f4-b7d9-0b67679a9187)
setting up the balancing conditions, which is to `maintain 60% cpu ultilization`
![hw30](https://github.com/V1rushB/test-repo/assets/137794637/54d85f35-266b-46c0-a308-5c5864f933d9)
![hw31](https://github.com/V1rushB/test-repo/assets/137794637/614c857c-a6fa-445f-bbd3-c0dbde8da328)
![hw32](https://github.com/V1rushB/test-repo/assets/137794637/201250c2-2759-4e3c-ae97-8241f510098b)
![HW33](https://github.com/V1rushB/test-repo/assets/137794637/78110cdb-1044-4186-8f3b-1dbca9bf2c6f)

it's time for us to test it now..
![HW34](https://github.com/V1rushB/test-repo/assets/137794637/a1ee3456-942c-4408-ba07-0e321f205ba0)
well, it's actually on and healthchecks looks good.
further checking we can run it through the load balancer:
![HW35](https://github.com/V1rushB/test-repo/assets/137794637/0fcc5fee-d5d6-48ce-874d-1cd208a72302)
welp still, cool.
