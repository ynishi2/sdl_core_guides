# 1.6. Behavior when the HU returns RPC error

## 1. Overview
This chapter describes the behavior when the SDL App terminates unexpectedly.

## 2. Background/Purpose/Reason for Standardization
Currently, the process of SDL Apps during an unexpected termination is an SDL standard behavior.
However, the process itself is not explictly defined in the SDL standard specifications.
Hence, the purpose of this document is to standardize such cases/issues using the TOYOTA specification, in order to be able to contribute to the SDL Ecosystem.

## 3. Function Details
### 3.1. Function Overview
If the SDL App that is running on mobile is terminated unexpectedly, the App Connection will be disconnected.
Then, the SDLCore on the HU detects that the connection has been disconnected, and sends RPC"UnregisterAppInterface" to the HMI.
The HMI receives the notification and displays an error message.
