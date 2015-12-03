# Style guidelines for contributing content

Follow these style guidelines when writing content:

- [Use sentence-style capitalization for titles and headings](#use-sentence-style-capitalization-for-titles-and-headings)
- [Use consistent text formatting](#use-consistent-text-formatting)
- [Write clear and consistent code examples](#write-clear-and-consistent-code-examples)
- [Use active voice](#use-active-voice)
- [Use present tense](#use-present-tense)
- [Write to the user by using second person and imperative mood](#write-to-the-user-by-using-second-person-and-imperative-mood)
- [Write clear and consistent step text](#write-clear-and-consistent-step-text)
- [Clarify pronouns such as *it*, *this*, *there*, and *that*](#clarify-pronouns)
- [Clarify gerunds and participles](#clarify-gerunds-and-participles)

## Use sentence-style capitalization for titles and headings

Use sentence-style capitalization for all titles and headings. In sentence-style capitalization, you capitalize only the first word of the title or heading, plus any proper nouns, proper adjectives, and terms that are always capitalized, such as some acronyms and abbreviations. If the title includes a colon, capitalize the first word that follows the colon, regardless of its part of speech. 

Following are some examples: 

- Preparing a cloud server to be a mail server
- Install or upgrade PHP 5.3 for CentOS 5.x
- Ubuntu Hardy: Using mod_python to serve your application
- PHP configuration limits for Cloud Sites
- Troubleshooting a Vyatta site-to-site VPN connection
- Differences between IMAP and POP

## Use consistent text formatting

Certain text should be formatted differently from the surrounding text to designate a special meaning or to make the text stand out to the user. Usually this formatting is accomplished by applying a different font treatment (such as bold, italics, or monospace). 

- For text you want to emphasize, use italics. Example: The offset _must_ be a multiple of the limit (or zero).

- For error messages, use monospace. Example: `The user does not have permission to perform this action.`

- For code examples, use monospace. Example: `$ grep "ftp" /etc/xinetd.d/* `

- For file, directory, and folder names, use bold. However, if these are shown as part of code, use monospace. Examples: Copy the **index.php** file from your computer to the **content** folder. The following example shows a basic configuration for the FTP service, in a file in the `/etc/xinetd.d` directory.

- For keyboard key names and combinations, use bold. Example: Press **Enter**. 

- For UI fields, use bold. Example: Select **Start > Control Panel**, and then click the **Mail** icon.

Additionally, format placeholder text as follows:

- Show placeholders in camelCase.
- If the authoring tool allows it, apply italics to placeholders; if not, enclose them in  angle brackets. For example, `<hostName>`. 

## Write clear and consistent code examples

Observe the following guidelines when creating blocks of code as input or output examples:

- Do not use screenshots to show code examples. Format them as blocks of code, in monospace, by using the appropriate markup in your authoring tool. 
 
- When showing input, include a command prompt (such as $).
 
- As often as necessary, show input and output in separate blocks and provide explanations for each. For example, if the input contains arguments or parameters, explain those. If the user should expect something specific in the output, or you want to show only part of lengthy output, provide an explanation. Provide your users the information that they need, and separate the input and output when it makes sense.

- When the command is simple, and there is nothing specific to say about the output, you can show the input and output in the same code block, as the user would actually see the code in their own terminal. The inclusion of the command prompt will differentiate the input from the output.
 
- Ensure that any placeholder text in code is obvious. If the authoring tool allows it, apply italics to placeholders; if not, enclose them in angle brackets. Show all placeholder text in camelCase.
 
- Follow the conventions of the programming language used and preserve the capitalization that the author of the code used.
 
- For readability, you can break up long lines of input into blocks by ending each line with a backslash. 
 
- If the input includes a list of arguments or parameters, show the important or relevant ones first, and group related ones. If no other order makes sense, use alphabetical order. If you explain the arguments or parameters in text, show them in the same order that they appear in the code block.

The following examples illustrates many many of these guidelines:

### Create a VM running a Docker host
1. Show all the available virtual machines (VMs) that are running Docker.

    `$ docker-machine ls`

    If you have not created any VMs yet, your output should look as follows:

    `NAME   ACTIVE   DRIVER   STATE   URL`

2. Create a VM that is running Docker.

    `$ docker-machine create --driver virtualbox test`

    The `--driver` flag indicates what type of driver the machine will run on. In this case, `virtualbox` indicates that the driver is Oracle VirtualBox. The final argument in the command gives the VM a name, in this case, `test`.

    The output should as follows:

    ```
    Creating VirtualBox VM...
    Creating SSH key...
    Starting VirtualBox VM...
    Starting VM...
    To see how to connect Docker to this machine, run: docker-machine env test
    ```

3. Run `docker-machine ls` again to see the VM that you created.

    The output should look as follows:

    ```    
    NAME             ACTIVE   DRIVER       STATE     URL                         SWARM
    test                      virtualbox   Running   tcp://192.168.99.101:237
    ```

## Use active voice

In general, write in *active* voice rather than *passive* voice. 

- Active voice identifies the agent of action as the subject of the verb—usually the user.
- Passive voice identifies the recipient (not the source) of the action as the subject of the verb.

Active-voice sentences clarify the performer of an action and are easier to understand than passive-voice sentences. Passive voice is usually less engaging and more complicated than active voice. When you use passive voice, the actions and responses of the software can be difficult to distinguish from those of the user. In addition, passive voice usually requires more words than active voice. 

Following are examples of active voice:

- After you install the software, start the computer.           
- Click **OK** to save the configuration.                           
- Create a server.                                              
- Rackspace products and services solve your business problems. 

## Use present tense

Users read documentation to perform tasks or gather information. For users, these activities take place in their present, so the present tense is appropriate in most cases. Additionally, present tense is easier to read than past or future tense.

Use future tense only when you need to emphasize that something will occur later (from the users' perspective). To easily find and remove instances of future tense, search for *will*. 

Following are examples of present tense:

- After you log in, your account begins the verification process.
- Any user with a Cloud account can provision multiple ServiceNet database instances.
- The product prompts you to verify the deletion.
- To back up Cloud Sites to Cloud Files by using this example, you create two cron jobs. One job backs up the cloud site and database, and the second job uploads the backup to Cloud Files.
- When the contract changes, Rackspace will notify users in release notes.

## Write to the user by using second person and imperative mood

Users are more engaged with documentation when you use second person (that is, you address the user as *you*). Second person promotes a friendly tone by addressing users directly. Using second person with the imperative mood (in which the subject *you* is understood) and active voice helps to eliminate wordiness and confusion about who or what initiates an action, especially in procedural steps. 

Using second person also avoids the use of gender-specific, third-person pronouns such as *he*, *she*, *his*, and *hers*. If you must use third person, use the pronouns *they* and *their*, but ensure that the pronoun matches the referenced noun in number.
 
Use first person plural pronouns (*we*, *our*) judiciously. These pronouns emphasize the writer or Rackspace rather than the user, so before you use them, consider whether second person or imperative mood is more "user friendly." However, use *we recommend* rather than *it is recommended* or *Rackspace recommends*. Also, you can use *we* in the place of *Rackspace* if necessary.

The first-person singular pronoun *I* is acceptable in the question part of FAQs and when authors of blogs or signed articles are describing their own actions or opinions. 

Avoid switching person (point of view) in the same document. Switching person is acceptable, however, in blog posts that use first-person singular but then switch to second person for instructional steps. 

## Write clear and consistent step text

When you are providing instructions to users, you should generally number the steps (unless you have just one step). For the steps, use the following guidelines. The guidelines are followed by an example:

- Write each step as a complete imperative sentence (that is, a sentence that starts with an imperative verb) and use ending punctuation. In steps, the focus is on the user, and the voice is active.

- Usually, include only a single action in each step. If two actions are closely related, such as opening a menu and selecting a command from the menu, you can include both actions in one step. 

- If a step specifies where to perform an action, state where to perform the action before describing the action. 

- If a step specifies a situation or a condition, state the situation or condition before describing the action.

- Do *not* include explanatory or reference information in the action part of a step. If needed, follow the step with one or more paragraphs that provide such information.

- Do *not* document system actions, responses, or results as steps. Put necessary statements in paragraphs following the steps to which they apply.

- Use screenshots sparingly. Screenshots can help to orient the user, but a screenshot of every field or dialog box is usually not necessary.

- To indicate that a step is optional, include *(Optional)*, in italics, as a qualifier at the beginning of the step. 

- If more than one method exists for completing an action, document only one method, usually the most efficient or preferred method.

### Create a cluster

1. Log in to the [Carina Control Panel](https://app.getcarina.com/?_ga=1.19747704.1992129593.1447799312).

2. On the Clusters page, click **Add Cluster**.

3. On the Create Cluster page, enter a name for the cluster. For example, `mycluster`.

4. To scale your cluster, select **Enable Autoscale**.

    For more information, see [Autoscaling resources in Carina](https://getcarina.com/docs/tutorials/autoscaling-carina/).

5. Click **Create Cluster**.

    After a few moments, your cluster reaches a status of **active**.

## Clarify pronouns such as *it*, *this*, *there*, and *that*

Pronouns are useful, but you must ensure that their antecedents (the words that they are used in place of) are clear, and that they (the pronouns) don’t contribute to vagueness and ambiguity. 

- **It**: Ensure that the antecedent of *it* is clear. If multiple singular nouns precede *it*, any of them could be the antecedent. Also, avoid using *it is* to begin a sentence. Such a construction hides the real subject of the sentence. 

- **This**: Avoid beginning a sentence with the pronoun *this*, unless you follow this with a noun to clarify its meaning. 

- **There**: Avoid using *there is* and *there are* as the subject of a sentence or clause. Using *there* shifts the focus away from the real subject and often uses unnecessary words.

- **That**: Avoid using *that* as a demonstrative pronoun (which stands in for or points to a noun). Instead, use it as an adjective and follow it with a noun. 

## Clarify gerunds and participles

Participles are verbs that end in *-ed* or *-ing* and act as modifiers. Gerunds are verbs that end in *-ing* and act as nouns. Both types of words are useful and acceptable, but confusion can arise if they are not placed precisely in a sentence. For example, the word *meeting* can be a gerund or a modifier (or even a noun) depending on its placement in a sentence. Clarify gerunds and participles as necessary.
