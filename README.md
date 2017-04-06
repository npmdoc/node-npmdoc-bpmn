# api documentation for  [bpmn (v0.2.2)](https://github.com/e2ebridge/bpmn#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-bpmn.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-bpmn) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-bpmn.svg)](https://travis-ci.org/npmdoc/node-npmdoc-bpmn)
#### BPMN 2.0 execution engine

[![NPM](https://nodei.co/npm/bpmn.png?downloads=true)](https://www.npmjs.com/package/bpmn)

[![apidoc](https://npmdoc.github.io/node-npmdoc-bpmn/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-bpmn_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-bpmn/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-bpmn/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-bpmn/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "support@e2ebridge.com"
    },
    "bugs": {
        "url": "https://github.com/e2ebridge/bpmn/issues"
    },
    "dependencies": {
        "async": "0.9.0",
        "bunyan": ">= 0.21.3",
        "e2e-transaction-logger": "~0.1.0",
        "jaguardb": ">= 0.1.3",
        "mongodb": ">= 1.3.10",
        "node-fs": ">= 0.1.5",
        "node-uuid": ">= 1.4.0",
        "restify": ">= 2.5.1",
        "sax": ">= 0.5.2",
        "underscore.string": "^2.3.3",
        "winston": ">= 0.7.1"
    },
    "description": "BPMN 2.0 execution engine",
    "devDependencies": {
        "commander": ">= 2.0.0",
        "istanbul": ">= 0.1.44",
        "nodeunit": ">= 0.7.4"
    },
    "directories": {},
    "dist": {
        "shasum": "6000ca09777e1e2d59f9625ec5e3fafb4043568e",
        "tarball": "https://registry.npmjs.org/bpmn/-/bpmn-0.2.2.tgz"
    },
    "gitHead": "2a339a4ea2edcddeeea7598f8758b77bfc81afe1",
    "homepage": "https://github.com/e2ebridge/bpmn#readme",
    "keywords": [
        "bpmn",
        "workflow",
        "process",
        "automation",
        "integration",
        "system integration"
    ],
    "license": "MIT",
    "main": "./lib/public.js",
    "maintainers": [
        {
            "name": "mrassinger",
            "email": "mrassinger@e2ebridge.com"
        },
        {
            "name": "cschmitt",
            "email": "cschmitt@e2ebridge.com"
        }
    ],
    "name": "bpmn",
    "optionalDependencies": {
        "e2e-transaction-logger": "~0.1.0",
        "mongodb": ">= 1.3.10"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/e2ebridge/bpmn.git"
    },
    "scripts": {},
    "version": "0.2.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module bpmn](#apidoc.module.bpmn)
1.  boolean <span class="apidocSignatureSpan">bpmn.</span>_initialising
1.  boolean <span class="apidocSignatureSpan">bpmn.</span>_initialized
1.  [function <span class="apidocSignatureSpan">bpmn.</span>ProcessManager (options)](#apidoc.element.bpmn.ProcessManager)
1.  [function <span class="apidocSignatureSpan">bpmn.</span>clearCache ()](#apidoc.element.bpmn.clearCache)
1.  [function <span class="apidocSignatureSpan">bpmn.</span>createUnmanagedCollaboratingProcesses (bpmnFilePath, callback)](#apidoc.element.bpmn.createUnmanagedCollaboratingProcesses)
1.  [function <span class="apidocSignatureSpan">bpmn.</span>createUnmanagedCollaboratingProcessesFromXML (bpmnXML, handler, callback)](#apidoc.element.bpmn.createUnmanagedCollaboratingProcessesFromXML)
1.  [function <span class="apidocSignatureSpan">bpmn.</span>createUnmanagedProcess (bpmnFilePath, callback)](#apidoc.element.bpmn.createUnmanagedProcess)
1.  [function <span class="apidocSignatureSpan">bpmn.</span>createUnmanagedProcessFromXML (bpmnXML, handler, callback)](#apidoc.element.bpmn.createUnmanagedProcessFromXML)
1.  [function <span class="apidocSignatureSpan">bpmn.</span>getBPMNDefinitions (bpmnFilePath, cache)](#apidoc.element.bpmn.getBPMNDefinitions)
1.  [function <span class="apidocSignatureSpan">bpmn.</span>mapName2HandlerName (bpmnName)](#apidoc.element.bpmn.mapName2HandlerName)
1.  object <span class="apidocSignatureSpan">bpmn.</span>ProcessManager.prototype
1.  object <span class="apidocSignatureSpan">bpmn.</span>_definitionsToInitialize
1.  object <span class="apidocSignatureSpan">bpmn.</span>_initialiseCallbacks
1.  object <span class="apidocSignatureSpan">bpmn.</span>_initializationError
1.  object <span class="apidocSignatureSpan">bpmn.</span>_persistency
1.  object <span class="apidocSignatureSpan">bpmn.</span>_processCache
1.  object <span class="apidocSignatureSpan">bpmn.</span>_processDefinitions
1.  object <span class="apidocSignatureSpan">bpmn.</span>_processHandlers
1.  object <span class="apidocSignatureSpan">bpmn.</span>client
1.  object <span class="apidocSignatureSpan">bpmn.</span>debugger
1.  object <span class="apidocSignatureSpan">bpmn.</span>find
1.  object <span class="apidocSignatureSpan">bpmn.</span>handler
1.  object <span class="apidocSignatureSpan">bpmn.</span>history
1.  object <span class="apidocSignatureSpan">bpmn.</span>logLevels
1.  object <span class="apidocSignatureSpan">bpmn.</span>logger
1.  object <span class="apidocSignatureSpan">bpmn.</span>manager
1.  object <span class="apidocSignatureSpan">bpmn.</span>process
1.  object <span class="apidocSignatureSpan">bpmn.</span>rest
1.  object <span class="apidocSignatureSpan">bpmn.</span>state
1.  object <span class="apidocSignatureSpan">bpmn.</span>timeouts

#### [module bpmn.ProcessManager](#apidoc.module.bpmn.ProcessManager)
1.  [function <span class="apidocSignatureSpan">bpmn.</span>ProcessManager (options)](#apidoc.element.bpmn.ProcessManager.ProcessManager)

#### [module bpmn.ProcessManager.prototype](#apidoc.module.bpmn.ProcessManager.prototype)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_afterInitialization (callback)](#apidoc.element.bpmn.ProcessManager.prototype._afterInitialization)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_createCollaboratingProcesses (processDescriptors, callback)](#apidoc.element.bpmn.ProcessManager.prototype._createCollaboratingProcesses)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_createSingleProcess (processId, processName, callback)](#apidoc.element.bpmn.ProcessManager.prototype._createSingleProcess)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_getAllProcesses (callback)](#apidoc.element.bpmn.ProcessManager.prototype._getAllProcesses)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_initialiseDefinition (processDefinition)](#apidoc.element.bpmn.ProcessManager.prototype._initialiseDefinition)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addBpmnFilePath (bpmnFilePath, processHandler)](#apidoc.element.bpmn.ProcessManager.prototype.addBpmnFilePath)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addBpmnXML (bpmnXml, processName, processHandler)](#apidoc.element.bpmn.ProcessManager.prototype.addBpmnXML)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addHandler (name, handler)](#apidoc.element.bpmn.ProcessManager.prototype.addHandler)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addHandlerFilePath (name, handlerFilePath)](#apidoc.element.bpmn.ProcessManager.prototype.addHandlerFilePath)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addHandlerString (name, handlerString)](#apidoc.element.bpmn.ProcessManager.prototype.addHandlerString)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>createProcess (descriptors, callback)](#apidoc.element.bpmn.ProcessManager.prototype.createProcess)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>createServer (options, restifyOptions)](#apidoc.element.bpmn.ProcessManager.prototype.createServer)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>findByName (processName, caseSensitive, callback)](#apidoc.element.bpmn.ProcessManager.prototype.findByName)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>findByProperty (query, callback)](#apidoc.element.bpmn.ProcessManager.prototype.findByProperty)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>findByState (stateName, callback)](#apidoc.element.bpmn.ProcessManager.prototype.findByState)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>get (processId, callback)](#apidoc.element.bpmn.ProcessManager.prototype.get)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>getAllProcesses (callback)](#apidoc.element.bpmn.ProcessManager.prototype.getAllProcesses)
1.  [function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>getDefinitionNames (callback)](#apidoc.element.bpmn.ProcessManager.prototype.getDefinitionNames)

#### [module bpmn.client](#apidoc.module.bpmn.client)
1.  [function <span class="apidocSignatureSpan">bpmn.client.</span>BPMNProcessClient (bpmnProcess)](#apidoc.element.bpmn.client.BPMNProcessClient)

#### [module bpmn.debugger](#apidoc.module.bpmn.debugger)
1.  [function <span class="apidocSignatureSpan">bpmn.debugger.</span>DebuggerInterface (url, fileName)](#apidoc.element.bpmn.debugger.DebuggerInterface)
1.  [function <span class="apidocSignatureSpan">bpmn.debugger.</span>createDebuggerInterface (node, fileName)](#apidoc.element.bpmn.debugger.createDebuggerInterface)
1.  [function <span class="apidocSignatureSpan">bpmn.debugger.</span>isDebuggerElement (node)](#apidoc.element.bpmn.debugger.isDebuggerElement)

#### [module bpmn.find](#apidoc.module.bpmn.find)
1.  [function <span class="apidocSignatureSpan">bpmn.find.</span>findByName (bpmnProcesses, processName, caseSensitive)](#apidoc.element.bpmn.find.findByName)
1.  [function <span class="apidocSignatureSpan">bpmn.find.</span>findByProperty (bpmnProcesses, query)](#apidoc.element.bpmn.find.findByProperty)
1.  [function <span class="apidocSignatureSpan">bpmn.find.</span>findByState (bpmnProcesses, stateName)](#apidoc.element.bpmn.find.findByState)

#### [module bpmn.handler](#apidoc.module.bpmn.handler)
1.  [function <span class="apidocSignatureSpan">bpmn.handler.</span>callHandler (name, process, data, handlerDoneCallback)](#apidoc.element.bpmn.handler.callHandler)
1.  [function <span class="apidocSignatureSpan">bpmn.handler.</span>getHandlerFileName (bpmnFilePath)](#apidoc.element.bpmn.handler.getHandlerFileName)
1.  [function <span class="apidocSignatureSpan">bpmn.handler.</span>getHandlerFromFile (bpmnFilePath)](#apidoc.element.bpmn.handler.getHandlerFromFile)
1.  [function <span class="apidocSignatureSpan">bpmn.handler.</span>getHandlerFromProcess (name, process)](#apidoc.element.bpmn.handler.getHandlerFromProcess)
1.  [function <span class="apidocSignatureSpan">bpmn.handler.</span>getHandlerFromString (moduleString)](#apidoc.element.bpmn.handler.getHandlerFromString)
1.  [function <span class="apidocSignatureSpan">bpmn.handler.</span>mapName2HandlerName (name)](#apidoc.element.bpmn.handler.mapName2HandlerName)
1.  string <span class="apidocSignatureSpan">bpmn.handler.</span>handlerNameSeparator

#### [module bpmn.history](#apidoc.module.bpmn.history)
1.  [function <span class="apidocSignatureSpan">bpmn.history.</span>BPMNProcessHistory (history)](#apidoc.element.bpmn.history.BPMNProcessHistory)
1.  [function <span class="apidocSignatureSpan">bpmn.history.</span>HistoryEntry (name, type, begin, end)](#apidoc.element.bpmn.history.HistoryEntry)
1.  [function <span class="apidocSignatureSpan">bpmn.history.</span>setDummyTimestampFunction ()](#apidoc.element.bpmn.history.setDummyTimestampFunction)
1.  [function <span class="apidocSignatureSpan">bpmn.history.</span>setTimestampFunction (getTimestampFunction)](#apidoc.element.bpmn.history.setTimestampFunction)

#### [module bpmn.logger](#apidoc.module.bpmn.logger)
1.  [function <span class="apidocSignatureSpan">bpmn.logger.</span>Logger (process, options)](#apidoc.element.bpmn.logger.Logger)
1.  object <span class="apidocSignatureSpan">bpmn.logger.</span>logLevels

#### [module bpmn.manager](#apidoc.module.bpmn.manager)
1.  [function <span class="apidocSignatureSpan">bpmn.manager.</span>ProcessManager (options)](#apidoc.element.bpmn.manager.ProcessManager)

#### [module bpmn.process](#apidoc.module.bpmn.process)
1.  [function <span class="apidocSignatureSpan">bpmn.process.</span>createBPMNProcess (id, processDefinition, eventHandler, persistency, parentProcess, parentToken, parentHistoryEntry, callback)](#apidoc.element.bpmn.process.createBPMNProcess)

#### [module bpmn.rest](#apidoc.module.bpmn.rest)
1.  [function <span class="apidocSignatureSpan">bpmn.rest.</span>clearReceivedMessageIds ()](#apidoc.element.bpmn.rest.clearReceivedMessageIds)
1.  [function <span class="apidocSignatureSpan">bpmn.rest.</span>createServer (manager, options, restifyOptions)](#apidoc.element.bpmn.rest.createServer)

#### [module bpmn.state](#apidoc.module.bpmn.state)
1.  [function <span class="apidocSignatureSpan">bpmn.state.</span>BPMNProcessState (state)](#apidoc.element.bpmn.state.BPMNProcessState)
1.  [function <span class="apidocSignatureSpan">bpmn.state.</span>CallActivityToken (flowObjectName, owningProcessId, calledProcessId)](#apidoc.element.bpmn.state.CallActivityToken)
1.  [function <span class="apidocSignatureSpan">bpmn.state.</span>Token (flowObjectName, owningProcessId)](#apidoc.element.bpmn.state.Token)

#### [module bpmn.timeouts](#apidoc.module.bpmn.timeouts)
1.  [function <span class="apidocSignatureSpan">bpmn.timeouts.</span>BPMNPendingTimerEvents (bpmnProcess)](#apidoc.element.bpmn.timeouts.BPMNPendingTimerEvents)



# <a name="apidoc.module.bpmn"></a>[module bpmn](#apidoc.module.bpmn)

#### <a name="apidoc.element.bpmn.ProcessManager"></a>[function <span class="apidocSignatureSpan">bpmn.</span>ProcessManager (options)](#apidoc.element.bpmn.ProcessManager)
- description and source-code
```javascript
ProcessManager = function (options){
    var self = this;

    options = options || {};

    self._processCache = {};

    self._initialized = true;
    self._initialising = false;
    self._initializationError = null;
    self._definitionsToInitialize = [];
    self._initialiseCallbacks = [];

    self._persistency = null;
    if (options.persistencyOptions) {
        self._persistency =  new Persistency(options.persistencyOptions);
        self._doneLoadingHandler = options.persistencyOptions.doneLoading;
        self._doneSavingHandler = options.persistencyOptions.doneSaving;
    }

    self._processHandlers = {};
    self._processDefinitions = {};


    if(!options.handlerFilePath){
        options.handlerFilePath = [];
    }

    if(!util.isArray(options.handlerFilePath)){
        options.handlerFilePath = [options.handlerFilePath];
    }

    options.handlerFilePath.forEach(function(handlerDescriptor){
        if(!handlerDescriptor.name || !handlerDescriptor.filePath){
            throw new Error("handlerFilePath needs a name and a filePath");
        }

        self.addHandlerFilePath(handlerDescriptor.name, handlerDescriptor.filePath);
    });


    if(!options.handler){
        options.handler = [];
    }

    if(!util.isArray(options.handler)){
        options.handler = [options.handler];
    }

    options.handler.forEach(function(handlerDescriptor){
        if(!handlerDescriptor.name || !handlerDescriptor.module){
            throw new Error("handler needs a name and a module");
        }

        self.addHandler(handlerDescriptor.name, handlerDescriptor.module);
    });

    if(!options.handlerString){
        options.handlerString = [];
    }

    if(!util.isArray(options.handlerString)){
        options.handlerString = [options.handlerString];
    }

    options.handlerString.forEach(function(handlerString){
        if(!handlerString.name || !handlerString.string){
            throw new Error("handlerString needs a name and a string");
        }

        self.addHandlerString(handlerString.name, handlerString.string);
    });


    if(!options.bpmnFilePath){
        options.bpmnFilePath = [];
    }

    if(!util.isArray(options.bpmnFilePath)){
        options.bpmnFilePath = [options.bpmnFilePath];
    }

    options.bpmnFilePath.forEach(function(filePath){
        self.addBpmnFilePath(filePath);
    });


    if(!options.bpmnXML){
        options.bpmnXML = [];
    }

    if(!util.isArray(options.bpmnXML)){
        options.bpmnXML = [options.bpmnXML];
    }

    options.bpmnXML.forEach(function(bpmnXML){
        if(!bpmnXML.name || !bpmnXML.xml){
            throw new Error("bpmnXML needs a name and a xml");
        }

        self.addBpmnXML(bpmnXML.xml, bpmnXML.name);
    });
}
```
- example usage
```shell
...
	bpmnProcess.removeLogTransport(winston.transports.File);

Managing processes
==================

Process managers are used to create multiple processes using the same definitions and find them back later.

    var manager = new bpmn.ProcessManager();

    manager.addBpmnFilePath("path/to/myProcess.bpmn");

    manager.createProcess("myId", function(err, myProcess){

// we start the process
myProcess.triggerEvent("MyStart");
...
```

#### <a name="apidoc.element.bpmn.clearCache"></a>[function <span class="apidocSignatureSpan">bpmn.</span>clearCache ()](#apidoc.element.bpmn.clearCache)
- description and source-code
```javascript
clearCache = function () {
    definitions.clearCache();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.createUnmanagedCollaboratingProcesses"></a>[function <span class="apidocSignatureSpan">bpmn.</span>createUnmanagedCollaboratingProcesses (bpmnFilePath, callback)](#apidoc.element.bpmn.createUnmanagedCollaboratingProcesses)
- description and source-code
```javascript
createUnmanagedCollaboratingProcesses = function (bpmnFilePath, callback) {
    var processes = {};
    var processDefinitions = definitions.getBPMNProcessDefinitions(bpmnFilePath);
    var handler = handlers.getHandlerFromFile(bpmnFilePath);

    async.eachSeries(processDefinitions, function(processDefinition, done) {
        bpmnProcesses.createBPMNProcess(null, processDefinition, handler, function(err, bpmnProcess){
            if(err){
                done(err);
            }
            processes[processDefinition.name] = bpmnProcess;
            done();
        });
    }, function(err){
        var clients = [];

        Object.keys(processes).forEach(function(name){
            var bpmnProcess = processes[name];

            var participants = bpmnProcess.getProcessDefinition().getCollaboratingParticipants();

            participants.forEach(function (participant) {
                bpmnProcess.addParticipant(participant.name, processes[participant.name]);
            });

            clients.push(bpmnProcess.processClient);
        });

        callback(err, clients);
    });
}
```
- example usage
```shell
...
BPMN also supports collaborating processes as depicted below.

![](https://raw.githubusercontent.com/e2ebridge/bpmn/master/examples/processes/collaboration.png)

These processes must be created together:

	// create collaborating processes
bpmn.createUnmanagedCollaboratingProcesses("my/collaboration/example.bpmn", function(err, collaboratingProcesses){

    // start the second process
    var secondProcess = collaboratingProcesses[1];
    secondProcess.triggerEvent("Start Event 2");

});
...
```

#### <a name="apidoc.element.bpmn.createUnmanagedCollaboratingProcessesFromXML"></a>[function <span class="apidocSignatureSpan">bpmn.</span>createUnmanagedCollaboratingProcessesFromXML (bpmnXML, handler, callback)](#apidoc.element.bpmn.createUnmanagedCollaboratingProcessesFromXML)
- description and source-code
```javascript
createUnmanagedCollaboratingProcessesFromXML = function (bpmnXML, handler, callback) {
    var processes = {};
    var processDefinitions = definitions.getBPMNDefinitionsFromXML(bpmnXML);

    if(typeof handler === 'string'){
        handler = handlers.getHandlerFromString(handler);
    }

    async.eachSeries(processDefinitions, function(processDefinition, done) {
        bpmnProcesses.createBPMNProcess(null, processDefinition, handler, function(err, bpmnProcess){
            if(err){
                done(err);
            }
            processes[processDefinition.name] = bpmnProcess;
            done();
        });
    }, function(err){
        var clients = [];

        Object.keys(processes).forEach(function(name){
            var bpmnProcess = processes[name];

            var participants = bpmnProcess.getProcessDefinition().getCollaboratingParticipants();

            participants.forEach(function (participant) {
                bpmnProcess.addParticipant(participant.name, processes[participant.name]);
            });

            clients.push(bpmnProcess.processClient);
        });

        callback(err, clients);
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.createUnmanagedProcess"></a>[function <span class="apidocSignatureSpan">bpmn.</span>createUnmanagedProcess (bpmnFilePath, callback)](#apidoc.element.bpmn.createUnmanagedProcess)
- description and source-code
```javascript
createUnmanagedProcess = function (bpmnFilePath, callback) {
    var processDefinition, error;
    var processDefinitions = definitions.getBPMNProcessDefinitions(bpmnFilePath);
    var handler = handlers.getHandlerFromFile(bpmnFilePath);

    if (processDefinitions.length === 1) {
        processDefinition = processDefinitions[0];
    } else {
        error = new Error("The BPMN file '" + bpmnFilePath + "'. contains more than one process definition. Use 'createCollaboratingProcesses
' instead of 'createProcess'");
        if(!callback) {
            throw error;
        } else {
            callback(error);
        }
    }

    bpmnProcesses.createBPMNProcess(null, processDefinition, handler, function(err, bpmnProcess){
        if(!callback){
            return;
        }

        callback(err, bpmnProcess.processClient);
    });

}
```
- example usage
```shell
...
![](https://raw.githubusercontent.com/e2ebridge/bpmn/master/examples/processes/task.png)

then this process can be created by


	var bpmn = require("bpmn");
	// We assume there is a myProcess.js besides myProcess.bpmn that contains the handlers
	bpmn.createUnmanagedProcess("path/to/myProcess.bpmn", function(err, myProcess){

        // we start the process
        myProcess.triggerEvent("MyStart");

	});

The handler file looks like:
...
```

#### <a name="apidoc.element.bpmn.createUnmanagedProcessFromXML"></a>[function <span class="apidocSignatureSpan">bpmn.</span>createUnmanagedProcessFromXML (bpmnXML, handler, callback)](#apidoc.element.bpmn.createUnmanagedProcessFromXML)
- description and source-code
```javascript
createUnmanagedProcessFromXML = function (bpmnXML, handler, callback) {
    var processDefinition, error;
    var processDefinitions = definitions.getBPMNDefinitionsFromXML(bpmnXML, "Standalone");

    if (processDefinitions.length === 1) {
        processDefinition = processDefinitions[0];
    } else {
        error = new Error("The BPMN XML contains more than one process definition. Use 'createCollaboratingProcesses' instead of
 'createProcess'");
        return callback(error);
    }

    if(typeof handler === 'string') {
        handler = handlers.getHandlerFromString(handler);
    }

    bpmnProcesses.createBPMNProcess(null, processDefinition, handler, function(err, bpmnProcess){
        callback(err, bpmnProcess.processClient);
    });

}
```
- example usage
```shell
...
    	// Called after MyEnd has been reached
    	done(data);
	};

Processes can also be created from an xml string instead of file. In this case the handler can be an object or a javascript string
 that would be parsed.


	bpmn.createUnmanagedProcessFromXML("<definitions ... </definitions>", "exports.MyStart = ...", function(err, myProcess){

        // we start the process
        myProcess.triggerEvent("MyStart");

	});
...
```

#### <a name="apidoc.element.bpmn.getBPMNDefinitions"></a>[function <span class="apidocSignatureSpan">bpmn.</span>getBPMNDefinitions (bpmnFilePath, cache)](#apidoc.element.bpmn.getBPMNDefinitions)
- description and source-code
```javascript
getBPMNDefinitions = function (bpmnFilePath, cache) {
    var bpmnDefinitions = null;
    if (cache) {
        bpmnDefinitions = definitions.getCachedBPMNDefinitions(bpmnFilePath);
    } else {
        bpmnDefinitions = definitions.getBPMNDefinitions(bpmnFilePath);
    }
    return bpmnDefinitions;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.mapName2HandlerName"></a>[function <span class="apidocSignatureSpan">bpmn.</span>mapName2HandlerName (bpmnName)](#apidoc.element.bpmn.mapName2HandlerName)
- description and source-code
```javascript
mapName2HandlerName = function (bpmnName) {
    return handlers.mapName2HandlerName(bpmnName);
}
```
- example usage
```shell
...
 * @private
 */
BPMNProcess.prototype._registerActivityEndEvents = function() {
    var self = this;

    self.on(ACTIVITY_END_EVENT, function(activityName, data) {
var currentToken, owningProcessId, currentProcess, currentFlowObject, activityEndHandlerIsDone;
var handlerName = handler.mapName2HandlerName(activityName) + activityEndHandlerPostfix;
var trx = self.currentTrx = null;

if(self.transactionLogger){
    trx = self.currentTrx = self.transactionLogger.startTransaction(self.processDefinition.name, 'PSTATE', 'TRANSITION', null, activityName
+'Done');
}

if (self.state.hasTokens(activityName)) {
...
```



# <a name="apidoc.module.bpmn.ProcessManager"></a>[module bpmn.ProcessManager](#apidoc.module.bpmn.ProcessManager)

#### <a name="apidoc.element.bpmn.ProcessManager.ProcessManager"></a>[function <span class="apidocSignatureSpan">bpmn.</span>ProcessManager (options)](#apidoc.element.bpmn.ProcessManager.ProcessManager)
- description and source-code
```javascript
ProcessManager = function (options){
    var self = this;

    options = options || {};

    self._processCache = {};

    self._initialized = true;
    self._initialising = false;
    self._initializationError = null;
    self._definitionsToInitialize = [];
    self._initialiseCallbacks = [];

    self._persistency = null;
    if (options.persistencyOptions) {
        self._persistency =  new Persistency(options.persistencyOptions);
        self._doneLoadingHandler = options.persistencyOptions.doneLoading;
        self._doneSavingHandler = options.persistencyOptions.doneSaving;
    }

    self._processHandlers = {};
    self._processDefinitions = {};


    if(!options.handlerFilePath){
        options.handlerFilePath = [];
    }

    if(!util.isArray(options.handlerFilePath)){
        options.handlerFilePath = [options.handlerFilePath];
    }

    options.handlerFilePath.forEach(function(handlerDescriptor){
        if(!handlerDescriptor.name || !handlerDescriptor.filePath){
            throw new Error("handlerFilePath needs a name and a filePath");
        }

        self.addHandlerFilePath(handlerDescriptor.name, handlerDescriptor.filePath);
    });


    if(!options.handler){
        options.handler = [];
    }

    if(!util.isArray(options.handler)){
        options.handler = [options.handler];
    }

    options.handler.forEach(function(handlerDescriptor){
        if(!handlerDescriptor.name || !handlerDescriptor.module){
            throw new Error("handler needs a name and a module");
        }

        self.addHandler(handlerDescriptor.name, handlerDescriptor.module);
    });

    if(!options.handlerString){
        options.handlerString = [];
    }

    if(!util.isArray(options.handlerString)){
        options.handlerString = [options.handlerString];
    }

    options.handlerString.forEach(function(handlerString){
        if(!handlerString.name || !handlerString.string){
            throw new Error("handlerString needs a name and a string");
        }

        self.addHandlerString(handlerString.name, handlerString.string);
    });


    if(!options.bpmnFilePath){
        options.bpmnFilePath = [];
    }

    if(!util.isArray(options.bpmnFilePath)){
        options.bpmnFilePath = [options.bpmnFilePath];
    }

    options.bpmnFilePath.forEach(function(filePath){
        self.addBpmnFilePath(filePath);
    });


    if(!options.bpmnXML){
        options.bpmnXML = [];
    }

    if(!util.isArray(options.bpmnXML)){
        options.bpmnXML = [options.bpmnXML];
    }

    options.bpmnXML.forEach(function(bpmnXML){
        if(!bpmnXML.name || !bpmnXML.xml){
            throw new Error("bpmnXML needs a name and a xml");
        }

        self.addBpmnXML(bpmnXML.xml, bpmnXML.name);
    });
}
```
- example usage
```shell
...
	bpmnProcess.removeLogTransport(winston.transports.File);

Managing processes
==================

Process managers are used to create multiple processes using the same definitions and find them back later.

    var manager = new bpmn.ProcessManager();

    manager.addBpmnFilePath("path/to/myProcess.bpmn");

    manager.createProcess("myId", function(err, myProcess){

// we start the process
myProcess.triggerEvent("MyStart");
...
```



# <a name="apidoc.module.bpmn.ProcessManager.prototype"></a>[module bpmn.ProcessManager.prototype](#apidoc.module.bpmn.ProcessManager.prototype)

#### <a name="apidoc.element.bpmn.ProcessManager.prototype._afterInitialization"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_afterInitialization (callback)](#apidoc.element.bpmn.ProcessManager.prototype._afterInitialization)
- description and source-code
```javascript
_afterInitialization = function (callback){
    if(this._initialized){
        return callback(this._initializationError);
    }

    this._initialiseCallbacks.push(callback);
}
```
- example usage
```shell
...
/**
 * @param {String} processId
 * @param {Function} callback
 */
ProcessManager.prototype.get = function get(processId, callback) {
    var self = this;

    this._afterInitialization(function(err){
        if(callback){
            callback(err, self._processCache[processId]);
        }
    });
};

/**
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype._createCollaboratingProcesses"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_createCollaboratingProcesses (processDescriptors, callback)](#apidoc.element.bpmn.ProcessManager.prototype._createCollaboratingProcesses)
- description and source-code
```javascript
_createCollaboratingProcesses = function (processDescriptors, callback) {
    var self = this;
    var processes = {};

    async.eachSeries(processDescriptors, function(processDescriptor, done) {

        self._createSingleProcess(processDescriptor.id, processDescriptor.name, function(err, bpmnProcess){
            if(err){
                done(err);
            }
            processes[processDescriptor.name] = bpmnProcess;
            done();
        });

    }, function(err){
        var results = [];

        Object.keys(processes).forEach(function(name){
            var bpmnProcess = processes[name];

            var participants = bpmnProcess.getProcessDefinition().getCollaboratingParticipants();

            participants.forEach(function (participant) {
                bpmnProcess.addParticipant(participant.name, processes[participant.name]);
            });

            results.push(bpmnProcess);
        });

        callback(err, results);
    });
}
```
- example usage
```shell
...
    err = new Error('id already used');
}
            });
            if(err){
return callback(err);
            }

            self._createCollaboratingProcesses(descriptors, function(err, bpmnProcesses){
if(err){
    return callback(err);
}

descriptors.forEach(function(descriptor){             // check if one of the ids is already used
    if(self._processCache[descriptor.id]){          // again because a process could have been created in between
        err = new Error('id already used');
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype._createSingleProcess"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_createSingleProcess (processId, processName, callback)](#apidoc.element.bpmn.ProcessManager.prototype._createSingleProcess)
- description and source-code
```javascript
_createSingleProcess = function (processId, processName, callback){
    createBPMNProcess(processId, this._processDefinitions[processName], this._processHandlers[processName], this._persistency, function
(err, bpmnProcess){
        callback(err, bpmnProcess);
    });
}
```
- example usage
```shell
...
                return;
            }

            self._processDefinitions[currentDefinition.name] = currentDefinition;

            async.each(documents, function(document, done){                                                         // for each
persisted document found

                self._createSingleProcess(document.processId, currentDefinition.name, function(err, bpmnProcess){       // create
 the process
if(err){
    return done(err);
}

if(self._processCache[bpmnProcess.getProcessId()]){                  // check if id already used
    return done(new Error('duplicated id in persisted data'));
}
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype._getAllProcesses"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_getAllProcesses (callback)](#apidoc.element.bpmn.ProcessManager.prototype._getAllProcesses)
- description and source-code
```javascript
_getAllProcesses = function (callback) {
    var self = this;
    var allProcessIds = Object.keys(this._processCache);

    if(!callback){
        return;
    }

    callback(null, allProcessIds.map(function(loadedProcessId) {
        return self._processCache[loadedProcessId];
    }));
}
```
- example usage
```shell
...


    this._afterInitialization(function(err){
        if (err) {
return callback(err);
        }

        self._getAllProcesses(function (err, bpmnProcesses) {
if (err) {
    return callback(err);
}

callback(null, bpmnProcesses.map(function (bpmnProcess) {
    return bpmnProcess.processClient;
}));
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype._initialiseDefinition"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>_initialiseDefinition (processDefinition)](#apidoc.element.bpmn.ProcessManager.prototype._initialiseDefinition)
- description and source-code
```javascript
_initialiseDefinition = function (processDefinition){
    var self = this;

    self._initializationError = null;
    self._initialized = false;

    self._definitionsToInitialize.push(processDefinition);

    if(!self._initialising){    // if already initialising we don't call next, the definition will be initialised after current
one.
        next();
    }

    /**
     * Called after all initializations are done.
     * @param err
     */
    function execCallbacks(err){
        self._definitionsToInitialize = [];

        self._initializationError = err;
        self._initialized = true;
        self._initialising = false;

        self._initialiseCallbacks.forEach(function(callback){   // call all waiting callbacks
            callback(err);
        });
    }

    function next(){
        self._initialising = true;

        if(self._definitionsToInitialize.length === 0){     // if all definitions have been initialized
            return execCallbacks();
        }

        var currentDefinition = self._definitionsToInitialize.pop();    // get the next definition

        if(self._processDefinitions[currentDefinition.name] ||      // if the definition already exist it means the processes were
 already loaded
                !self._persistency){                                // if there is no persistency nothing needs to be loaded

            self._processDefinitions[currentDefinition.name] = currentDefinition;   // we simply add or replace the definition
            return next();
        }


        self._persistency.loadAll(currentDefinition.name, function(err, documents){     // load all saved document

            if(err){
                execCallbacks(err);
                return;
            }

            self._processDefinitions[currentDefinition.name] = currentDefinition;

            async.each(documents, function(document, done){                                                         // for each
persisted document found

                self._createSingleProcess(document.processId, currentDefinition.name, function(err, bpmnProcess){       // create
 the process
                    if(err){
                        return done(err);
                    }

                    if(self._processCache[bpmnProcess.getProcessId()]){                  // check if id already used
                        return done(new Error('duplicated id in persisted data'));
                    }

                    self._processCache[bpmnProcess.getProcessId()] = bpmnProcess;
                    done();
                });

            }, function(err){
                if(err){
                    return execCallbacks(err);
                }

                next();
            });

        });

    }

}
```
- example usage
```shell
...

       if(processHandler) {
           self._processHandlers[processDefinition.name] = processHandler;
       } else if(!self._processHandlers[processDefinition.name]){
           throw new Error('No process handler defined for process "'+processDefinition.name+'". The process handler must be defined
 before the process or with the process.');
       }

       self._initialiseDefinition(processDefinition);
   });
};

/**
* Add a bpmn XML to the manager.
* All process definition found in this file will be initialized and replace the old ones if exists.
* A process handler object or file path can be passed. If none passed the same file path as the bpmn is used or the existing handler
.
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.addBpmnFilePath"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addBpmnFilePath (bpmnFilePath, processHandler)](#apidoc.element.bpmn.ProcessManager.prototype.addBpmnFilePath)
- description and source-code
```javascript
addBpmnFilePath = function (bpmnFilePath, processHandler){
    var self = this;
    var processDefinitions;

    if(typeof processHandler === 'string'){
        processHandler = handlers.getHandlerFromFile(processHandler);
    }

    if(!processHandler){
        try{
            processHandler = handlers.getHandlerFromFile(bpmnFilePath);
            processHandler.doneLoadingHandler = self._doneLoadingHandler;
            processHandler.doneSavingHandler = self._doneSavingHandler;
        }catch(err){}
    }

    processDefinitions = definitions.getBPMNProcessDefinitions(bpmnFilePath);

    processDefinitions.forEach(function(processDefinition){

        if(processHandler) {
            self._processHandlers[processDefinition.name] = processHandler;
        } else if(!self._processHandlers[processDefinition.name]){
            throw new Error('No process handler defined for process "'+processDefinition.name+'". The process handler must be defined
 before the process or with the process.');
        }

        self._initialiseDefinition(processDefinition);
    });
}
```
- example usage
```shell
...
Managing processes
==================

Process managers are used to create multiple processes using the same definitions and find them back later.

var manager = new bpmn.ProcessManager();

manager.addBpmnFilePath("path/to/myProcess.bpmn");

manager.createProcess("myId", function(err, myProcess){

    // we start the process
    myProcess.triggerEvent("MyStart");

});
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.addBpmnXML"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addBpmnXML (bpmnXml, processName, processHandler)](#apidoc.element.bpmn.ProcessManager.prototype.addBpmnXML)
- description and source-code
```javascript
addBpmnXML = function (bpmnXml, processName, processHandler){
    var self = this;
    var processDefinitions;

    if(typeof processHandler === 'string'){
        processHandler = handlers.getHandlerFromString(processHandler);
    }

    processDefinitions = definitions.getBPMNDefinitionsFromXML(bpmnXml, processName);

    processDefinitions.forEach(function(processDefinition){

        if(processHandler) {
            self._processHandlers[processDefinition.name] = processHandler;
        } else if(!self._processHandlers[processDefinition.name]){
            throw new Error('No process handler defined for process "'+processDefinition.name+'". The process handler must be defined
 before the process or with the process.');
        }

        self._initialiseDefinition(processDefinition);
    });
}
```
- example usage
```shell
...
   }

   options.bpmnXML.forEach(function(bpmnXML){
       if(!bpmnXML.name || !bpmnXML.xml){
           throw new Error("bpmnXML needs a name and a xml");
       }

       self.addBpmnXML(bpmnXML.xml, bpmnXML.name);
   });
};

/**
* Initialise a new definition by loading all persisted process.
* All other function that need the initialise state will wait until initialization is done.
*
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.addHandler"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addHandler (name, handler)](#apidoc.element.bpmn.ProcessManager.prototype.addHandler)
- description and source-code
```javascript
addHandler = function (name, handler){
    this._processHandlers[name] = handler;
    this._processHandlers[name].doneLoadingHandler = this._doneLoadingHandler || this._processHandlers[name].doneLoadingHandler;
    this._processHandlers[name].doneSavingHandler = this._doneSavingHandler || this._processHandlers[name].doneSavingHandler;
}
```
- example usage
```shell
...
}

options.handler.forEach(function(handlerDescriptor){
    if(!handlerDescriptor.name || !handlerDescriptor.module){
        throw new Error("handler needs a name and a module");
    }

    self.addHandler(handlerDescriptor.name, handlerDescriptor.module);
});

if(!options.handlerString){
    options.handlerString = [];
}

if(!util.isArray(options.handlerString)){
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.addHandlerFilePath"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addHandlerFilePath (name, handlerFilePath)](#apidoc.element.bpmn.ProcessManager.prototype.addHandlerFilePath)
- description and source-code
```javascript
addHandlerFilePath = function (name, handlerFilePath){
    this._processHandlers[name] = handlers.getHandlerFromFile(handlerFilePath);
    this._processHandlers[name].doneLoadingHandler = this._doneLoadingHandler || this._processHandlers[name].doneLoadingHandler;
    this._processHandlers[name].doneSavingHandler = this._doneSavingHandler || this._processHandlers[name].doneSavingHandler;
}
```
- example usage
```shell
...

    var manager = new bpmn.ProcessManager({
        bpmnFilePath: "path/to/myProcess.bpmn"
    });



ProcessManager.addHandlerFilePath(name, handlerFilePath)

- **name**: The name of the process definition for which the handler will be used.
- **handlerFilePath**: Path to the javascript file defining the handler module.

ProcessManager.addHandlerString = function(name, handlerString)

- **name**: The name of the process definition for which the handler will be used.
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.addHandlerString"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>addHandlerString (name, handlerString)](#apidoc.element.bpmn.ProcessManager.prototype.addHandlerString)
- description and source-code
```javascript
addHandlerString = function (name, handlerString){
    this._processHandlers[name] = handlers.getHandlerFromString(handlerString);
    this._processHandlers[name].doneLoadingHandler = this._doneLoadingHandler || this._processHandlers[name].doneLoadingHandler;
    this._processHandlers[name].doneSavingHandler = this._doneSavingHandler || this._processHandlers[name].doneSavingHandler;
}
```
- example usage
```shell
...
}

options.handlerString.forEach(function(handlerString){
    if(!handlerString.name || !handlerString.string){
        throw new Error("handlerString needs a name and a string");
    }

    self.addHandlerString(handlerString.name, handlerString.string);
});


if(!options.bpmnFilePath){
    options.bpmnFilePath = [];
}
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.createProcess"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>createProcess (descriptors, callback)](#apidoc.element.bpmn.ProcessManager.prototype.createProcess)
- description and source-code
```javascript
createProcess = function (descriptors, callback) {
    var self = this;

    this._afterInitialization(function(err){
        if(err){
            return callback(err);
        }

        if (typeof descriptors === 'string' && Object.keys(self._processDefinitions).length !== 1) {
            return callback(new Error("The manager contains more than one process definition. " +
                "processId have to be an Array.<{name: String, id: String}>} "));
        }

        if(util.isArray(descriptors)) {
            descriptors.forEach(function(descriptor){             // check if one of the ids is already used
                if(self._processCache[descriptor.id]){
                    err = new Error('id already used');
                }
            });
            if(err){
                return callback(err);
            }

            self._createCollaboratingProcesses(descriptors, function(err, bpmnProcesses){
                if(err){
                    return callback(err);
                }

                descriptors.forEach(function(descriptor){             // check if one of the ids is already used
                    if(self._processCache[descriptor.id]){          // again because a process could have been created in between
                        err = new Error('id already used');
                    }
                });
                if(err){
                    return callback(err);
                }

                callback(null, bpmnProcesses.map(function(bpmnProcess){
                    self._processCache[bpmnProcess.getProcessId()] = bpmnProcess;
                    return bpmnProcess.processClient;
                }));
            });

            return;
        }

        if(typeof descriptors === 'string') {
            descriptors = {
                id: descriptors,
                name: Object.keys(self._processDefinitions)[0]
            };
        }

        if(self._processCache[descriptors.id]){                                        // check if id already used
            return callback(new Error('id already used'));
        }

        self._createSingleProcess(descriptors.id, descriptors.name, function(err, bpmnProcess){
            if(err){
                return callback(err);
            }

            if(self._processCache[descriptors.id]){                                      // check if id already used
                return callback(new Error('id already used'));                      // again because a process could have been created
 in between
            }

            self._processCache[descriptors.id] = bpmnProcess;
            callback(null, bpmnProcess.processClient);
        });
    });
}
```
- example usage
```shell
...

Process managers are used to create multiple processes using the same definitions and find them back later.

    var manager = new bpmn.ProcessManager();

    manager.addBpmnFilePath("path/to/myProcess.bpmn");

    manager.createProcess("myId", function(err, myProcess){

        // we start the process
        myProcess.triggerEvent("MyStart");

    });

If the process id is already used an error is returned.
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.createServer"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>createServer (options, restifyOptions)](#apidoc.element.bpmn.ProcessManager.prototype.createServer)
- description and source-code
```javascript
createServer = function (options, restifyOptions){
    return rest.createServer(this,  options, restifyOptions);
}
```
- example usage
```shell
...

Server
------

The above API can also be called by REST HTTP calls. To do this, you have first to instantiate a server from ta manager. For example
:

	// Returns a restify server.
	var server = manager.createServer();
	server.listen(9009, function() {
    	console.log('%s listening at %s', server.name, server.url);
	});

The server is a node restify server. So all features of this package can be used.
The full signature of 'createProcess'  is
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.findByName"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>findByName (processName, caseSensitive, callback)](#apidoc.element.bpmn.ProcessManager.prototype.findByName)
- description and source-code
```javascript
findByName = function (processName, caseSensitive, callback) {
    var self = this;

    if(typeof caseSensitive === 'function'){
        callback = caseSensitive;
        caseSensitive = true;
    }

    if(!callback){
        return;
    }

    this._afterInitialization(function(err){
        if (err) {
            return callback(err);
        }

        self.getAllProcesses(function (err, bpmnProcesses) {
            if (err) {
                return callback(err);
            }

            callback(null, find.findByName(bpmnProcesses, processName, caseSensitive));
        });
    });
}
```
- example usage
```shell
...

	// returns all processes in this state (callActivity, tasks, event, ...)
	bpmn.findByState(stateName, function(err, processes){
        ...
    });

	// returns all processes using this definition
	bpmn.findByName(definitionName, function(err, processes){
        ...
    });


Persistency
-----------
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.findByProperty"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>findByProperty (query, callback)](#apidoc.element.bpmn.ProcessManager.prototype.findByProperty)
- description and source-code
```javascript
findByProperty = function (query, callback) {
    var self = this;

    if(!callback){
        return;
    }

    this._afterInitialization(function(err){
        if (err) {
            return callback(err);
        }

        self.getAllProcesses(function (err, bpmnProcesses) {
            if (err) {
                return callback(err);
            }

            callback(null, find.findByProperty(bpmnProcesses, query));
        });
    });
}
```
- example usage
```shell
...

	// returns all processes
bpmn.getAllProcesses(function(err, processes){
    ...
});

	// returns all processes having the property names
	bpmn.findByProperty({propName1: propValue1, propName2: propValue2, ...}, function(err, processes){
    ...
});

	// returns all processes in this state (callActivity, tasks, event, ...)
	bpmn.findByState(stateName, function(err, processes){
    ...
});
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.findByState"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>findByState (stateName, callback)](#apidoc.element.bpmn.ProcessManager.prototype.findByState)
- description and source-code
```javascript
findByState = function (stateName, callback) {
    var self = this;

    if(!callback){
        return;
    }

    this._afterInitialization(function(err){
        if (err) {
            return callback(err);
        }

        self.getAllProcesses(function (err, bpmnProcesses) {
            if (err) {
                return callback(err);
            }

            callback(null, find.findByState(bpmnProcesses, stateName));
        });
    });
}
```
- example usage
```shell
...

	// returns all processes having the property names
	bpmn.findByProperty({propName1: propValue1, propName2: propValue2, ...}, function(err, processes){
    ...
});

	// returns all processes in this state (callActivity, tasks, event, ...)
	bpmn.findByState(stateName, function(err, processes){
    ...
});

	// returns all processes using this definition
	bpmn.findByName(definitionName, function(err, processes){
    ...
});
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.get"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>get (processId, callback)](#apidoc.element.bpmn.ProcessManager.prototype.get)
- description and source-code
```javascript
function get(processId, callback) {
    var self = this;

    this._afterInitialization(function(err){
        if(callback){
            callback(err, self._processCache[processId]);
        }
    });
}
```
- example usage
```shell
...

Finding processes
-----------------

Existing processes in a manager can be retrived using these functions:

	// returns the process with the corresponding id
	bpmn.get(processId, function(err, process){
    ...
	});

	// returns all processes
bpmn.getAllProcesses(function(err, processes){
    ...
});
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.getAllProcesses"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>getAllProcesses (callback)](#apidoc.element.bpmn.ProcessManager.prototype.getAllProcesses)
- description and source-code
```javascript
getAllProcesses = function (callback) {
    var self = this;

    if(!callback){
        return;
    }


    this._afterInitialization(function(err){
        if (err) {
            return callback(err);
        }

        self._getAllProcesses(function (err, bpmnProcesses) {
            if (err) {
                return callback(err);
            }

            callback(null, bpmnProcesses.map(function (bpmnProcess) {
                return bpmnProcess.processClient;
            }));
        });
    });
}
```
- example usage
```shell
...

	// returns the process with the corresponding id
	bpmn.get(processId, function(err, process){
    ...
	});

	// returns all processes
bpmn.getAllProcesses(function(err, processes){
    ...
});

	// returns all processes having the property names
	bpmn.findByProperty({propName1: propValue1, propName2: propValue2, ...}, function(err, processes){
    ...
});
...
```

#### <a name="apidoc.element.bpmn.ProcessManager.prototype.getDefinitionNames"></a>[function <span class="apidocSignatureSpan">bpmn.ProcessManager.prototype.</span>getDefinitionNames (callback)](#apidoc.element.bpmn.ProcessManager.prototype.getDefinitionNames)
- description and source-code
```javascript
getDefinitionNames = function (callback){
    var self = this;

    this._afterInitialization(function(err){
        callback(err, Object.keys(self._processDefinitions));
    });
}
```
- example usage
```shell
...
 * @param {ProcessManager} manager
 * @param {String} name
 * @param {Function} callback
 * @returns {*}
 */
function getNameWithCase(manager, name, callback){

    manager.getDefinitionNames(function(err, names){
if(err){
    return callback(err);
}

var ret = null;

names.forEach(function(nameWithCase){
...
```



# <a name="apidoc.module.bpmn.client"></a>[module bpmn.client](#apidoc.module.bpmn.client)

#### <a name="apidoc.element.bpmn.client.BPMNProcessClient"></a>[function <span class="apidocSignatureSpan">bpmn.client.</span>BPMNProcessClient (bpmnProcess)](#apidoc.element.bpmn.client.BPMNProcessClient)
- description and source-code
```javascript
BPMNProcessClient = function (bpmnProcess) {
    this._implementation = bpmnProcess;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bpmn.debugger"></a>[module bpmn.debugger](#apidoc.module.bpmn.debugger)

#### <a name="apidoc.element.bpmn.debugger.DebuggerInterface"></a>[function <span class="apidocSignatureSpan">bpmn.debugger.</span>DebuggerInterface (url, fileName)](#apidoc.element.bpmn.debugger.DebuggerInterface)
- description and source-code
```javascript
DebuggerInterface = function (url, fileName) {
    this.fileName = fileName;
    this.url = urls.parse(url);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.debugger.createDebuggerInterface"></a>[function <span class="apidocSignatureSpan">bpmn.debugger.</span>createDebuggerInterface (node, fileName)](#apidoc.element.bpmn.debugger.createDebuggerInterface)
- description and source-code
```javascript
createDebuggerInterface = function (node, fileName) {
    return (new DebuggerInterface(parserUtils.getAttributesValue(node, "href"), fileName));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.debugger.isDebuggerElement"></a>[function <span class="apidocSignatureSpan">bpmn.debugger.</span>isDebuggerElement (node)](#apidoc.element.bpmn.debugger.isDebuggerElement)
- description and source-code
```javascript
isDebuggerElement = function (node) {
    return (node.uri === 'http://e2e.ch/bpmneditor/debugger' && node.local === 'position');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bpmn.find"></a>[module bpmn.find](#apidoc.module.bpmn.find)

#### <a name="apidoc.element.bpmn.find.findByName"></a>[function <span class="apidocSignatureSpan">bpmn.find.</span>findByName (bpmnProcesses, processName, caseSensitive)](#apidoc.element.bpmn.find.findByName)
- description and source-code
```javascript
findByName = function (bpmnProcesses, processName, caseSensitive) {
    var foundProcesses = [];

    if (processName) {
        var compare = function(a, b) {
            var result;
            if (caseSensitive === undefined || caseSensitive) {
                result = (a === b);
            } else {
                result = (a.toLowerCase() === b.toLowerCase());
            }
            return result;
        };

        bpmnProcesses.forEach(function(bpmnProcess) {
            var name = bpmnProcess.getProcessDefinition().name;
            if (compare(name, processName)) {
                foundProcesses.push(bpmnProcess.processClient || bpmnProcess);
            }
        });
    }
    return foundProcesses;
}
```
- example usage
```shell
...

	// returns all processes in this state (callActivity, tasks, event, ...)
	bpmn.findByState(stateName, function(err, processes){
        ...
    });

	// returns all processes using this definition
	bpmn.findByName(definitionName, function(err, processes){
        ...
    });


Persistency
-----------
...
```

#### <a name="apidoc.element.bpmn.find.findByProperty"></a>[function <span class="apidocSignatureSpan">bpmn.find.</span>findByProperty (bpmnProcesses, query)](#apidoc.element.bpmn.find.findByProperty)
- description and source-code
```javascript
findByProperty = function (bpmnProcesses, query) {
    var foundProcesses = [];
    var findAll = !query;

    bpmnProcesses.forEach(function(bpmnProcess) {
        if (findAll || hasMatchingProperties(bpmnProcess.getProperties(), query)) {
            foundProcesses.push(bpmnProcess.processClient || bpmnProcess);
        }
    });
    return foundProcesses;
}
```
- example usage
```shell
...

	// returns all processes
bpmn.getAllProcesses(function(err, processes){
    ...
});

	// returns all processes having the property names
	bpmn.findByProperty({propName1: propValue1, propName2: propValue2, ...}, function(err, processes){
    ...
});

	// returns all processes in this state (callActivity, tasks, event, ...)
	bpmn.findByState(stateName, function(err, processes){
    ...
});
...
```

#### <a name="apidoc.element.bpmn.find.findByState"></a>[function <span class="apidocSignatureSpan">bpmn.find.</span>findByState (bpmnProcesses, stateName)](#apidoc.element.bpmn.find.findByState)
- description and source-code
```javascript
findByState = function (bpmnProcesses, stateName) {
    var foundProcesses = [];
    var findAll = !stateName;

    bpmnProcesses.forEach(function(bpmnProcess) {
        if (findAll || bpmnProcess.getState().hasTokens(stateName)) {
            foundProcesses.push(bpmnProcess.processClient || bpmnProcess);
        }
    });
    return foundProcesses;
}
```
- example usage
```shell
...

	// returns all processes having the property names
	bpmn.findByProperty({propName1: propValue1, propName2: propValue2, ...}, function(err, processes){
    ...
});

	// returns all processes in this state (callActivity, tasks, event, ...)
	bpmn.findByState(stateName, function(err, processes){
    ...
});

	// returns all processes using this definition
	bpmn.findByName(definitionName, function(err, processes){
    ...
});
...
```



# <a name="apidoc.module.bpmn.handler"></a>[module bpmn.handler](#apidoc.module.bpmn.handler)

#### <a name="apidoc.element.bpmn.handler.callHandler"></a>[function <span class="apidocSignatureSpan">bpmn.handler.</span>callHandler (name, process, data, handlerDoneCallback)](#apidoc.element.bpmn.handler.callHandler)
- description and source-code
```javascript
callHandler = function (name, process, data, handlerDoneCallback) {
    var result, handlerType;
    var done = handlerDoneCallback || function() {};
    var eventType = "callHandler";
    var handler = getHandlerFromProcess(name, process);

    if (handler) {
        handlerType = typeof handler;
        if (handlerType === 'function') {
            try {
                result = handler.call(process.processClient, data, done);
            } catch (error) {
                process.logger.error("Error in handler '" + name + "': " + error.toString());
                process.defaultErrorHandler.call(process.processClient, error, done);
            }
        } else if (handlerType === 'object') {
            // hierarchical handler used for mocking up sub process handlers. See test cases for examples
            // To keep going we have to call done()
            done();
        } else {
            process.callDefaultEventHandler(eventType, name, mapName2HandlerName(name),
                                            "Unknown handler type: '" + handlerType + "'", done);
        }
     } else {
        process.callDefaultEventHandler(eventType, name, mapName2HandlerName(name), "No handler found", done);
    }

    return result;
}
```
- example usage
```shell
...
            trx.processStateEnd(self.processDefinition.name, self.getProcessId(), activityName);
            trx.end();
        }
        self.logger.trace("Calling done() of '" + handlerName + "'.");
        currentProcess._emitTokens(currentFlowObject, data, true);
    };
    self.logger.trace("Calling '" + handlerName + "' for " + ACTIVITY_END_EVENT + " '" + activityName + "'.");
    handler.callHandler(handlerName, currentProcess, data, activityEndHandlerIsDone);
} else {
    self.callDefaultEventHandler(ACTIVITY_END_EVENT, activityName, handlerName,
        "Process cannot handle this activity because it is not currently executed.",
        function(){
            if(trx){
                trx.end();
            }
...
```

#### <a name="apidoc.element.bpmn.handler.getHandlerFileName"></a>[function <span class="apidocSignatureSpan">bpmn.handler.</span>getHandlerFileName (bpmnFilePath)](#apidoc.element.bpmn.handler.getHandlerFileName)
- description and source-code
```javascript
getHandlerFileName = function (bpmnFilePath) {
    return (fileUtils.removeFileExtension(bpmnFilePath) + ".js");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.handler.getHandlerFromFile"></a>[function <span class="apidocSignatureSpan">bpmn.handler.</span>getHandlerFromFile (bpmnFilePath)](#apidoc.element.bpmn.handler.getHandlerFromFile)
- description and source-code
```javascript
getHandlerFromFile = function (bpmnFilePath) {
    var handlerFilePath = getHandlerFileName(bpmnFilePath);
    return require(handlerFilePath);
}
```
- example usage
```shell
...
/**
* Change the process handler using a file.
*
* @param {String} name Name of the process
* @param {String} handlerFilePath
*/
ProcessManager.prototype.addHandlerFilePath = function(name, handlerFilePath){
   this._processHandlers[name] = handlers.getHandlerFromFile(handlerFilePath);
   this._processHandlers[name].doneLoadingHandler = this._doneLoadingHandler || this._processHandlers[name].doneLoadingHandler;
   this._processHandlers[name].doneSavingHandler = this._doneSavingHandler || this._processHandlers[name].doneSavingHandler;
};

/**
* Change the process handler using a string.
*
...
```

#### <a name="apidoc.element.bpmn.handler.getHandlerFromProcess"></a>[function <span class="apidocSignatureSpan">bpmn.handler.</span>getHandlerFromProcess (name, process)](#apidoc.element.bpmn.handler.getHandlerFromProcess)
- description and source-code
```javascript
getHandlerFromProcess = function (name, process) {
    var handlerName = mapName2HandlerName(name);
    var handler = process.eventHandler[handlerName]; // this works as long as event names are unique
    return handler;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.handler.getHandlerFromString"></a>[function <span class="apidocSignatureSpan">bpmn.handler.</span>getHandlerFromString (moduleString)](#apidoc.element.bpmn.handler.getHandlerFromString)
- description and source-code
```javascript
getHandlerFromString = function (moduleString) {
    var Module = require('module').Module;
    var handlerModule = new Module();
    handlerModule._compile(stripBOM(moduleString));
    return handlerModule.exports;
}
```
- example usage
```shell
...
/**
* Change the process handler using a string.
*
* @param {String} name Name of the process
* @param {String} handlerString
*/
ProcessManager.prototype.addHandlerString = function(name, handlerString){
   this._processHandlers[name] = handlers.getHandlerFromString(handlerString);
   this._processHandlers[name].doneLoadingHandler = this._doneLoadingHandler || this._processHandlers[name].doneLoadingHandler;
   this._processHandlers[name].doneSavingHandler = this._doneSavingHandler || this._processHandlers[name].doneSavingHandler;
};

/**
* Change the process handler using an object.
*
...
```

#### <a name="apidoc.element.bpmn.handler.mapName2HandlerName"></a>[function <span class="apidocSignatureSpan">bpmn.handler.</span>mapName2HandlerName (name)](#apidoc.element.bpmn.handler.mapName2HandlerName)
- description and source-code
```javascript
mapName2HandlerName = function (name) {
    var cleanName = name.replace(/[:!'~\^@*#¢¬ç?¦\|&;%@"<>\(\){}\[\]\+, \t\n]/g, "_");

    if (cleanName.match(/^[0-9]/)) {
        cleanName = "_" + cleanName;
    }
    return cleanName;
}
```
- example usage
```shell
...
 * @private
 */
BPMNProcess.prototype._registerActivityEndEvents = function() {
    var self = this;

    self.on(ACTIVITY_END_EVENT, function(activityName, data) {
var currentToken, owningProcessId, currentProcess, currentFlowObject, activityEndHandlerIsDone;
var handlerName = handler.mapName2HandlerName(activityName) + activityEndHandlerPostfix;
var trx = self.currentTrx = null;

if(self.transactionLogger){
    trx = self.currentTrx = self.transactionLogger.startTransaction(self.processDefinition.name, 'PSTATE', 'TRANSITION', null, activityName
+'Done');
}

if (self.state.hasTokens(activityName)) {
...
```



# <a name="apidoc.module.bpmn.history"></a>[module bpmn.history](#apidoc.module.bpmn.history)

#### <a name="apidoc.element.bpmn.history.BPMNProcessHistory"></a>[function <span class="apidocSignatureSpan">bpmn.history.</span>BPMNProcessHistory (history)](#apidoc.element.bpmn.history.BPMNProcessHistory)
- description and source-code
```javascript
BPMNProcessHistory = function (history) {
    /** @type {Array.<HistoryEntry>} */
    this.historyEntries = [];

    if (history) {
        this.historyEntries = history.historyEntries.map(function(historyEntry) {
            var entry = new HistoryEntry(historyEntry.name, historyEntry.type, historyEntry.begin, historyEntry.end);
            if (historyEntry.subhistory) {
                entry.subhistory = new BPMNProcessHistory(historyEntry.subhistory);
            }
            return entry;
        });
        this.createdAt = history.createdAt;
        this.finishedAt = history.finishedAt || null;
    } else {
        this.createdAt = getTimestamp();
        this.finishedAt = null;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.history.HistoryEntry"></a>[function <span class="apidocSignatureSpan">bpmn.history.</span>HistoryEntry (name, type, begin, end)](#apidoc.element.bpmn.history.HistoryEntry)
- description and source-code
```javascript
HistoryEntry = function (name, type, begin, end) {
    this.name = name;
    this.type = type;
    this.begin = begin || getTimestamp();
    this.end = end || null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.history.setDummyTimestampFunction"></a>[function <span class="apidocSignatureSpan">bpmn.history.</span>setDummyTimestampFunction ()](#apidoc.element.bpmn.history.setDummyTimestampFunction)
- description and source-code
```javascript
setDummyTimestampFunction = function () {
    getTimestamp = function () { return "_dummy_ts_"; };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.history.setTimestampFunction"></a>[function <span class="apidocSignatureSpan">bpmn.history.</span>setTimestampFunction (getTimestampFunction)](#apidoc.element.bpmn.history.setTimestampFunction)
- description and source-code
```javascript
setTimestampFunction = function (getTimestampFunction) {
    getTimestamp = getTimestampFunction;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bpmn.logger"></a>[module bpmn.logger](#apidoc.module.bpmn.logger)

#### <a name="apidoc.element.bpmn.logger.Logger"></a>[function <span class="apidocSignatureSpan">bpmn.logger.</span>Logger (process, options)](#apidoc.element.bpmn.logger.Logger)
- description and source-code
```javascript
Logger = function (process, options) {
    this.logLevel = logLevels.error;
    if (options) {
        this.logLevel = getLogLevelValue(options.logLevel || this.logLevel);
    }

    /** {function(string)} */
    this.logAppender = null; // used for example to test log messages

    this.winstonFileTransport = new (winston.transports.File)({
        //level: getLogLevelString(this.logLevel), //TODO: this should work, but it doesn't. Why?
        level: 'verbose',
        filename: './process.log',
        maxsize: 64 * 1024 * 1024,
        maxFiles: 100,
        timestamp: function() {
            return Date.now();
        }
    });
    this.winstonConsoleTransport = new (winston.transports.Console)({
        //level: getLogLevelString(this.logLevel), //TODO: this should work, but it doesn't. Why?
        level: 'verbose',
        colorize: true,
        json: false
    });
    this.winstonLogger = new (winston.Logger)({
        transports: [this.winstonFileTransport, this.winstonConsoleTransport],
        levels: logLevels,
        colors: logLevelColors
    });

    this.setProcess(process);
}
```
- example usage
```shell
...
this.persistency = persistency;
this.deferredEvents = [];
this.deferEvents = false; // events must be deferred if the process engine is loading or saving state
this.processClient = new BPMNProcessClient(this);
this.participants = {}; // if the process takes part in a collaboration, we store all participant process in this map
this.properties = {}; // TODO: how do we handle parent data?
this.calledProcesses = {};
this.logger = new log.Logger(this, {logLevel: log.logLevels.error});
if(transactionLog) {
    this.transactionLogger = new transactionLog.TransactionLogger();
}
this.currentTrx = null;
this.views = {
    startEvent : null,
    endEvent : null,
...
```



# <a name="apidoc.module.bpmn.manager"></a>[module bpmn.manager](#apidoc.module.bpmn.manager)

#### <a name="apidoc.element.bpmn.manager.ProcessManager"></a>[function <span class="apidocSignatureSpan">bpmn.manager.</span>ProcessManager (options)](#apidoc.element.bpmn.manager.ProcessManager)
- description and source-code
```javascript
ProcessManager = function (options){
    var self = this;

    options = options || {};

    self._processCache = {};

    self._initialized = true;
    self._initialising = false;
    self._initializationError = null;
    self._definitionsToInitialize = [];
    self._initialiseCallbacks = [];

    self._persistency = null;
    if (options.persistencyOptions) {
        self._persistency =  new Persistency(options.persistencyOptions);
        self._doneLoadingHandler = options.persistencyOptions.doneLoading;
        self._doneSavingHandler = options.persistencyOptions.doneSaving;
    }

    self._processHandlers = {};
    self._processDefinitions = {};


    if(!options.handlerFilePath){
        options.handlerFilePath = [];
    }

    if(!util.isArray(options.handlerFilePath)){
        options.handlerFilePath = [options.handlerFilePath];
    }

    options.handlerFilePath.forEach(function(handlerDescriptor){
        if(!handlerDescriptor.name || !handlerDescriptor.filePath){
            throw new Error("handlerFilePath needs a name and a filePath");
        }

        self.addHandlerFilePath(handlerDescriptor.name, handlerDescriptor.filePath);
    });


    if(!options.handler){
        options.handler = [];
    }

    if(!util.isArray(options.handler)){
        options.handler = [options.handler];
    }

    options.handler.forEach(function(handlerDescriptor){
        if(!handlerDescriptor.name || !handlerDescriptor.module){
            throw new Error("handler needs a name and a module");
        }

        self.addHandler(handlerDescriptor.name, handlerDescriptor.module);
    });

    if(!options.handlerString){
        options.handlerString = [];
    }

    if(!util.isArray(options.handlerString)){
        options.handlerString = [options.handlerString];
    }

    options.handlerString.forEach(function(handlerString){
        if(!handlerString.name || !handlerString.string){
            throw new Error("handlerString needs a name and a string");
        }

        self.addHandlerString(handlerString.name, handlerString.string);
    });


    if(!options.bpmnFilePath){
        options.bpmnFilePath = [];
    }

    if(!util.isArray(options.bpmnFilePath)){
        options.bpmnFilePath = [options.bpmnFilePath];
    }

    options.bpmnFilePath.forEach(function(filePath){
        self.addBpmnFilePath(filePath);
    });


    if(!options.bpmnXML){
        options.bpmnXML = [];
    }

    if(!util.isArray(options.bpmnXML)){
        options.bpmnXML = [options.bpmnXML];
    }

    options.bpmnXML.forEach(function(bpmnXML){
        if(!bpmnXML.name || !bpmnXML.xml){
            throw new Error("bpmnXML needs a name and a xml");
        }

        self.addBpmnXML(bpmnXML.xml, bpmnXML.name);
    });
}
```
- example usage
```shell
...
	bpmnProcess.removeLogTransport(winston.transports.File);

Managing processes
==================

Process managers are used to create multiple processes using the same definitions and find them back later.

    var manager = new bpmn.ProcessManager();

    manager.addBpmnFilePath("path/to/myProcess.bpmn");

    manager.createProcess("myId", function(err, myProcess){

// we start the process
myProcess.triggerEvent("MyStart");
...
```



# <a name="apidoc.module.bpmn.process"></a>[module bpmn.process](#apidoc.module.bpmn.process)

#### <a name="apidoc.element.bpmn.process.createBPMNProcess"></a>[function <span class="apidocSignatureSpan">bpmn.process.</span>createBPMNProcess (id, processDefinition, eventHandler, persistency, parentProcess, parentToken, parentHistoryEntry, callback)](#apidoc.element.bpmn.process.createBPMNProcess)
- description and source-code
```javascript
createBPMNProcess = function (id, processDefinition, eventHandler, persistency, parentProcess, parentToken, parentHistoryEntry, callback) {
    var bpmnProcess;

    if(typeof persistency === 'function' ){
        callback = persistency;
        persistency = null;
        parentProcess = null;
        parentToken = null;
        parentHistoryEntry = null;
    } else if(typeof parentProcess === 'function' ){
        callback = parentProcess;
        parentProcess = null;
        parentToken = null;
        parentHistoryEntry = null;
    } else if(typeof parentToken === 'function' ){
        callback = parentToken;
        parentToken = null;
        parentHistoryEntry = null;
    } else if(typeof parentHistoryEntry === 'function' ){
        callback = parentHistoryEntry;
        parentHistoryEntry = null;
    }

    if(!callback){
        return;
    }

    bpmnProcess = new BPMNProcess(id, processDefinition, eventHandler, persistency, parentProcess, parentToken, parentHistoryEntry
);

    if (bpmnProcess.isMainProcess()) {
        // we save all process information - including called processes - in one document
        bpmnProcess.loadPersistedData(function(err){
            if(callback){
                callback(err, bpmnProcess);
            }
        });
    } else {
        if(callback){
            process.nextTick(function(){        // to stay consistent
                callback(null, bpmnProcess);
            });
        }
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bpmn.rest"></a>[module bpmn.rest](#apidoc.module.bpmn.rest)

#### <a name="apidoc.element.bpmn.rest.clearReceivedMessageIds"></a>[function <span class="apidocSignatureSpan">bpmn.rest.</span>clearReceivedMessageIds ()](#apidoc.element.bpmn.rest.clearReceivedMessageIds)
- description and source-code
```javascript
clearReceivedMessageIds = function () {
    receivedMessageIds = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.rest.createServer"></a>[function <span class="apidocSignatureSpan">bpmn.rest.</span>createServer (manager, options, restifyOptions)](#apidoc.element.bpmn.rest.createServer)
- description and source-code
```javascript
createServer = function (manager, options, restifyOptions) {
    var logger, serverOptions, server;
    var settings = options || {};

    settings.createProcessId = settings.createProcessId || uuid.v1;

    logger = new log.Logger(null, settings);
    serverOptions = restifyOptions || {};
    serverOptions.name = serverOptions.name || "BPMNProcessServer";

    // Shimming the log doesn't work as expected: I cannot switch it off for example.
    // Additionally, the log format is horrible. So for the time being we use our own logging
    // serverOptions.log = serverOptions.log || bunyan2winston.createLogger(logger.winstonLogger);

    server = restify.createServer(serverOptions);

    server.use(restify.queryParser({ mapParams: false }));
    server.use(restify.bodyParser({ mapParams: false }));
    server.on('after', function( request, response, route, error) {
        var handler = options.onServerAfterEvent || onServerAfterEvent;
        handler(logger, request, response, route, error);
    });

    server.get(getProcessRoute,
        transactionLog.transactionLoggerMiddleware({
                name: function(req){
                    return 'GET ' + req.params.processName + ' process';
                }
            }),
        function(req, res, next){
            getProcess(manager, req, res, next);
        });
    server.get(getProcessesRoute,
        transactionLog.transactionLoggerMiddleware({
            name: function(req){
                return 'GET ' + req.params.processName + ' processes';
            }
        }),
        function(req, res, next){
            getProcesses(manager, req, res, next);
        });
    server.put(sendMessageRoute,
        transactionLog.transactionLoggerMiddleware({
            name: function(req){
                return 'PUT ' + req.params.messageName + ' message to ' + req.params.processName + ' process';
            }
        }),
        function(req, res, next) {
            sendMessage(manager, logger, req, res, next);
        }
    );

    // TODO: we need to change these routes.  the catch all '/' makes this load order dependent.
    server.post(createAndStartCollaboratingProcessRoute,
      transactionLog.transactionLoggerMiddleware({
        name: function(req) {
          return 'POST create and start collaborating processes';
        }
      }),
      function(req, res, next) {
        createAndStartCollaboratingProcess(manager, settings, logger, req, res, next);
      }
    );

    server.post(createProcessRoute,
        transactionLog.transactionLoggerMiddleware({
            name: function(req){
                return 'POST create ' + req.params.processName + ' process';
            }
        }),
        function(req, res, next) {
            createProcess(manager, settings, logger, req, res, next);
}
    );
    server.post(createAndStartProcessRoute,
        transactionLog.transactionLoggerMiddleware({
            name: function(req){
                return 'POST create and start ' + req.params.processName + ' process';
            }
        }),
        function(req, res, next) {
            createAndStartProcess(manager, settings, logger, req, res, next);
        }
    );

    return server;
}
```
- example usage
```shell
...

Server
------

The above API can also be called by REST HTTP calls. To do this, you have first to instantiate a server from ta manager. For example
:

	// Returns a restify server.
	var server = manager.createServer();
	server.listen(9009, function() {
    	console.log('%s listening at %s', server.name, server.url);
	});

The server is a node restify server. So all features of this package can be used.
The full signature of 'createProcess'  is
...
```



# <a name="apidoc.module.bpmn.state"></a>[module bpmn.state](#apidoc.module.bpmn.state)

#### <a name="apidoc.element.bpmn.state.BPMNProcessState"></a>[function <span class="apidocSignatureSpan">bpmn.state.</span>BPMNProcessState (state)](#apidoc.element.bpmn.state.BPMNProcessState)
- description and source-code
```javascript
BPMNProcessState = function (state) {
    /** @type {Array.<Token>} */
    this.tokens = state && state.tokens ? state.tokens : [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.state.CallActivityToken"></a>[function <span class="apidocSignatureSpan">bpmn.state.</span>CallActivityToken (flowObjectName, owningProcessId, calledProcessId)](#apidoc.element.bpmn.state.CallActivityToken)
- description and source-code
```javascript
CallActivityToken = function (flowObjectName, owningProcessId, calledProcessId) {
    Token.call(this, flowObjectName, owningProcessId);
    this.substate = null;
    this.calledProcessId = calledProcessId;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.bpmn.state.Token"></a>[function <span class="apidocSignatureSpan">bpmn.state.</span>Token (flowObjectName, owningProcessId)](#apidoc.element.bpmn.state.Token)
- description and source-code
```javascript
Token = function (flowObjectName, owningProcessId) {
    this.position = flowObjectName;
    this.owningProcessId = owningProcessId;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.bpmn.timeouts"></a>[module bpmn.timeouts](#apidoc.module.bpmn.timeouts)

#### <a name="apidoc.element.bpmn.timeouts.BPMNPendingTimerEvents"></a>[function <span class="apidocSignatureSpan">bpmn.timeouts.</span>BPMNPendingTimerEvents (bpmnProcess)](#apidoc.element.bpmn.timeouts.BPMNPendingTimerEvents)
- description and source-code
```javascript
BPMNPendingTimerEvents = function (bpmnProcess) {
    /** @type {Array.<Timeout>} */
    this.pendingTimeouts = {};
    this.bpmnProcess = bpmnProcess;
    this.setTimeoutIds = {};
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
