# EasyCommands
Public library to make slash commands creation for JDA API easier.

## Example Main class setup.

    public static void main(String[] args) throws InterruptedException {

        JDABuilder jdaBuilder = JDABuilder.create("---", Arrays.asList(EasyCommands.gatewayIntents));
        
        jdaBuilder.enableCache(Arrays.asList(EasyCommands.cacheFlags));

        JDA jda = jdaBuilder.build().awaitReady();

        EasyCommands easyCommands = new EasyCommands(jda, useDevCommands?); // If you don't know how to use devCommands you can set it to 'false'

        easyCommands.addExecutor(new HelpCmd(), new OtherCmdEx(), etc);
        easyCommands.enableMusicBot();
        easyCommands.registerListeners(
            //Your Listeners in here (ListenerAdpaters)
            new Example1(),
            new Example2(),
            ...
        );
    }

## Download
### Current latest version: 0.3

    <dependency>
        <groupId>ca.tristan.jdaeasycommands</groupId>
        <artifactId>jdaeasycommands</artifactId>
        <version>VERSION</version>
    </dependency>
