reading the config file that contains the ports and path to the files to serve -> listening on the port waiting for a request -> establishing a tcp connection with the user -> receiving the http msg and parse it -> routing -> app handler -> returning the response with the status code.

Handle many clients at the same time using non-blocking I/O, using multithreading (a thread only to receive the stram of http byte stream, a thread for parsing the requestand adding it to the queue)

making sure the program (server) never crash unexpectedly.