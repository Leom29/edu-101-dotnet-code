# Exercise 4: Finale Workflow

One of the benefits of Temporal is that it provides SDKs for several
languages and you can use multiple languages in the context of a single
Workflow. For example, you might write your Workflow in TypeScript but use
Java or Go for an Activity in that workflow.

The last exercise in this workshop does exactly that. The Workflow
itself is written in TypeScript, but the Activity that is executed as part
of this Workflow is written in Java, as is the Worker that runs it.
Since the Activity is written in Java, it's able to use a Java graphics
library that would otherwise be would be incompatible with a typical
TypeScript program.

# Start the Worker (Java)

In one terminal, run the following command:

```
java -classpath \
java-activity-and-worker.jar \
io.temporal.training.PdfCertWorker
```

# Edit the Workflow (dotnet)

Open the [Program.cs](./src/Client/Program.cs) file, and change the argument passed to the Workflow from 'Maxim Fateev' to your name.

# Start the Workflow (dotnet)

Run the command below from another terminal to start the Workflow:

```sh
dotnet run --project ./exercises/finaleworkflow/src/Client/Client.csproj
```

- Once the Workflow is complete, use the explorer
  view on the left side of the exercise environment
  to locate the file created by this workflow. It
  will have a name similar to `101_certificate_maxim_fateev.pdf`,
  only with your name in place of `maxim_fateev`.
- Right-click its icon in the explorer view and choose
  **Download...**.
- After you've downloading it to your
  computer, open it with your preferred PDF viewer.

Thank you for participating in Temporal 101!

### This is the end of the exercise.
