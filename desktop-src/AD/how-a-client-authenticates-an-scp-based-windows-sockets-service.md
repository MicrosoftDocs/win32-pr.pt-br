---
title: Como um cliente autentica um serviço Windows Sockets baseado em SCP
description: Este tópico mostra o código que um aplicativo cliente usa para compor um SPN para um serviço.
ms.assetid: b5ef79c6-e321-435c-b3de-817fdea8836a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38471f48d8c80d0795b7176b95df0029d42325ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453502"
---
# <a name="how-a-client-authenticates-an-scp-based-windows-sockets-service"></a>Como um cliente autentica um serviço Windows Sockets baseado em SCP

Este tópico mostra o código que um aplicativo cliente usa para compor um SPN para um serviço. O cliente é associado ao SCP (ponto de conexão de serviço) do serviço para recuperar os dados necessários para se conectar ao serviço. O SCP também contém dados que o cliente pode usar para compor o SPN do serviço. Para obter mais informações e um exemplo de código que se associa ao SCP e recupera as propriedades necessárias, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md).

Este tópico também mostra como um cliente usa um pacote de segurança SSPI e o SPN do serviço para estabelecer uma conexão mutuamente autenticada com o serviço Windows Sockets. Lembre-se de que esse código é quase idêntico ao código necessário no Microsoft Windows NT 4,0 e anterior apenas para autenticar o cliente no servidor. A única diferença é que o cliente deve fornecer o SPN e especificar o \_ sinalizador de \_ autenticação mútua do ISC req \_ .

## <a name="client-code-to-make-an-spn-for-a-service"></a>Código do cliente para criar um SPN para um serviço


```C++
// Initialize these strings by querying the service's SCP.
TCHAR szDn[MAX_PATH],     // DN of the service's SCP.
      szServer[MAX_PATH], // DNS name of the service's server.
      szClass[MAX_PATH];  // Service class.
 
TCHAR szSpn[MAX_PATH];    // Buffer for SPN.
SOCKET sockServer;        // Socket connected to service.
DWORD dwRes, dwLen;
.
.
.
// Compose the SPN for the service using the DN, Class, and Server
// returned by ScpLocate.
dwLen = sizeof(szSpn);
dwRes = DsMakeSpn(
     szClass,    // Service class.
     szDn,       // DN of the service's SCP.
     szServer,   // DNS name of the server on which service is running.
     0,          // No port component in SPN.
     NULL,       // No referrer.
     &dwLen,     // Size of szSpn buffer.
     szSpn);     // Buffer to receive the SPN.

if (!DoAuthentication (sockServer, szSpn)) {
    closesocket (sockServer);
    return(FALSE);
}
.
.
.
```



## <a name="client-code-to-authenticate-the-service"></a>Código do cliente para autenticar o serviço

Este exemplo de código consiste em duas rotinas: **doauthentication** e **GenClientContext**. Depois de chamar [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) para compor um SPN para o serviço, o cliente passa o SPN para a rotina **doauthentication** , que chama o **GenClientContext** para gerar o buffer inicial a ser enviado ao serviço. O **doauthentication** usa o identificador de soquete para enviar o buffer e receber a resposta do serviço passada para o pacote SSPI por outra chamada para **GenClientContext**. Esse loop é repetido até que a autenticação falhe ou **GenClientContext** defina um sinalizador que indica a autenticação bem-sucedida.

A rotina **GenClientContext** interage com o pacote SSPI para gerar os dados de autenticação a serem enviados ao serviço e processar os dados recebidos do serviço. Os principais componentes dos dados de autenticação fornecidos pelo cliente incluem:

-   O nome da entidade de serviço que identifica as credenciais que o serviço deve autenticar.
-   As credenciais do cliente. A função [**falha AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) do pacote de segurança extrai essas credenciais do contexto de segurança do cliente estabelecido no logon.
-   Para solicitar a autenticação mútua, o cliente deve especificar o \_ sinalizador de autenticação mútua do ISC req \_ \_ ao chamar a função [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) durante a rotina **GenClientContext** .


```C++
// Structure for storing the state of the authentication sequence.
typedef struct _AUTH_SEQ 
{
    BOOL _fNewConversation;
    CredHandle _hcred;
    BOOL _fHaveCredHandle;
    BOOL _fHaveCtxtHandle;
    struct _SecHandle  _hctxt;
} AUTH_SEQ, *PAUTH_SEQ;
 
/***************************************************************/
//   DoAuthentication routine for the client.
//
//   Manages the client's authentication conversation with the service 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL DoAuthentication (
        SOCKET s, 
        LPTSTR szSpn)
{
BOOL done = FALSE;
DWORD cbOut, cbIn;
 
// Call the security package to generate the initial buffer of 
// authentication data to send to the service.
cbOut = g_cbMaxMessage;
if (!GenClientContext (s, NULL, 0, g_pOutBuf, 
                       &cbOut, &done, szSpn))
    return(FALSE);
    
if (!SendMsg (s, g_pOutBuf, cbOut))
    return(FALSE);
 
// Pass the service's response back to the security package, and send 
// the package's output back to the service. Repeat until complete.
while (!done) 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenClientContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                           &cbOut, &done, szSpn))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
}
 
return(TRUE);
}
 
/***************************************************************/
//   GenClientContext routine
//
//   Handles the client's interactions with the security package.
//   Optionally takes an input buffer coming from the service 
//   and generates a buffer of data to send back to the 
//   service. Also returns an indication when the authentication
//   is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenClientContext (
            DWORD dwKey,     // Socket handle used as key.
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone,
            LPTSTR szSpn)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes;
PAUTH_SEQ        pAS; // Structure to store state of authentication.
 
// Get structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
            NULL,    // Principal
            PACKAGE_NAME,
            SECPKG_CRED_OUTBOUND,
            NULL,    // LOGON id
            NULL,    // Authentication data
            NULL,    // Get key function.
            NULL,    // Get key argument.
            &pAS->_hcred,
            &Lifetime
            );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else 
    {
        fprintf (stderr, 
                 "AcquireCredentialsHandle failed: %u\n", ssStatus);
        return(FALSE);
    }
}
 
// Prepare output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers = 1;
OutBuffDesc.pBuffers = &OutSecBuff;
 
OutSecBuff.cbBuffer = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer = pOut;
 
// Prepare input buffer.
if (!pAS->_fNewConversation) 
{
    InBuffDesc.ulVersion = 0;
    InBuffDesc.cBuffers = 1;
    InBuffDesc.pBuffers = &InSecBuff;
 
    InSecBuff.cbBuffer = cbIn;
    InSecBuff.BufferType = SECBUFFER_TOKEN;
    InSecBuff.pvBuffer = pIn;
}
 
_tprintf(TEXT("InitializeSecurityContext: pszTarget=%s\n"),szSpn);
 
ssStatus = g_pFuncs->InitializeSecurityContext (
                     &pAS->_hcred,
                     pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                     szSpn,
                     ISC_REQ_MUTUAL_AUTH,      // Context requirements
                     0,                        // Reserved1
                     SECURITY_NATIVE_DREP,
                     pAS->_fNewConversation ? NULL : &InBuffDesc,
                     0,                        // Reserved2
                     &pAS->_hctxt,
                     &OutBuffDesc,
                     &ContextAttributes,
                     &Lifetime
                     );
if (!SEC_SUCCESS (ssStatus)) 
{
    fprintf (stderr, "init context failed: %X\n", ssStatus);
    return FALSE;
}
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete token if applicable.
if ( (SEC_I_COMPLETE_NEEDED == ssStatus) || 
     (SEC_I_COMPLETE_AND_CONTINUE == ssStatus))  
{
    if (g_pFuncs->CompleteAuthToken) 
    {
        ssStatus = g_pFuncs->CompleteAuthToken (&pAS->_hctxt, 
                                                &OutBuffDesc);
        if (!SEC_SUCCESS(ssStatus)) 
        {
            fprintf (stderr, "complete failed: %u\n", ssStatus);
            return FALSE;
        }
    } else 
    {
        fprintf (stderr, "Complete not supported.\n");
        return FALSE;
    }
}
 
*pcbOut = OutSecBuff.cbBuffer;
 
if (pAS->_fNewConversation)
    pAS->_fNewConversation = FALSE;
 
*pfDone = !((SEC_I_CONTINUE_NEEDED == ssStatus) ||
            (SEC_I_COMPLETE_AND_CONTINUE == ssStatus));
 
// Check the ISC_RET_MUTUAL_AUTH flag to verify that 
// mutual authentication was performed.
if (*pfDone && !(ContextAttributes && ISC_RET_MUTUAL_AUTH) )
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
return TRUE;
}
```



 

 




