---
title: Como um serviço do Windows Sockets autentica um cliente
description: Quando um cliente se conecta ao serviço Windows Sockets, o serviço inicia suas operações para a sequência de autenticação mútua, que é mostrada nos exemplos de código a seguir.
ms.assetid: 32f62fb9-41c6-4932-9b91-753174919707
ms.tgt_platform: multiple
keywords:
- Como um serviço do Windows Sockets autentica um AD do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad096ddfb9569d6289c1e775465232431c20ad6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917124"
---
# <a name="how-a-windows-sockets-service-authenticates-a-client"></a>Como um serviço do Windows Sockets autentica um cliente

Quando um cliente se conecta ao serviço Windows Sockets, o serviço inicia suas operações para a sequência de autenticação mútua, que é mostrada nos exemplos de código a seguir.

A rotina **doauthentication** usa o identificador de soquete para receber o primeiro pacote de autenticação do cliente. O buffer do cliente é passado para a função **GenServerContext** , que então passa o buffer para o pacote de segurança SSPI para autenticação. A **doautenticação** envia a saída do pacote de segurança de volta para o cliente. Esse loop é repetido até que a autenticação falhe ou **GenServerContext** defina um sinalizador indicando que a autenticação foi bem-sucedida.

**GenServerContext** chama as seguintes funções de um pacote de segurança SSPI:

-   [**Falha AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) extrai as credenciais de serviço do contexto de segurança do serviço que foi estabelecido quando o serviço foi iniciado.
-   O [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) tenta executar a autenticação mútua usando as credenciais de serviço e os dados de autenticação recebidos do cliente. Para solicitar a autenticação mútua, a chamada **AcceptSecurityContext** deve especificar o \_ \_ sinalizador de autenticação mútua do ASC req \_ .
-   [**CompleteAuthToken**](/windows/desktop/api/sspi/nf-sspi-completeauthtoken) é chamado, se necessário, para concluir a operação de autenticação.

O exemplo de código a seguir usa o pacote Negotiate da biblioteca Secur32.dll de pacotes de segurança.


```C++
/***************************************************************/
//   DoAuthentication routine for the service
//
//   Manages the service authentication communication with the client 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication succeeds.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
 
BOOL DoAuthentication (SOCKET s)
{
DWORD cbIn, cbOut;
BOOL done = FALSE;

if(s==INVALID_SOCKET)
{
    return(FALSE);
}
 
// Receive authentication data from the client and pass
// it to the security package. Send the package output back
// to the client. Repeat until complete.
do 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenServerContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                               &cbOut, &done))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
} 
while(!done);
 
return(TRUE);
}
 
/***************************************************************/
//   GenServerContext routine 
//
//   Handles the service interactions with the security package.
//   Takes an input buffer coming from the client and generates a 
//   buffer of data to send back to the client. Also returns 
//   an indication when the authentication is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenServerContext (
            DWORD dwKey,
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes = 0;
PAUTH_SEQ        pAS = null;

if((pIn==NULL && cbIn>0) || (pOut==NULL) || (pcbOut==NULL) || (pfDone==NULL))
{
    return(FALSE);
}
 
// Get a structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)  
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
                        NULL,    // principal
                        PACKAGE_NAME,
                        SECPKG_CRED_INBOUND,
                        NULL,    // LOGON id
                        NULL,    // authentication data
                        NULL,    // get key function
                        NULL,    // get key argument
                        &pAS->_hcred,
                        &Lifetime
                        );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else
    {
        fprintf (stderr, "AcquireCredentialsHandle failed: %u\n", 
                 ssStatus);
        return(FALSE);
    }
}
 
// Prepare the output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers  = 1;
OutBuffDesc.pBuffers  = &OutSecBuff;
 
OutSecBuff.cbBuffer   = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer   = pOut;
 
// Prepare the input buffer.
InBuffDesc.ulVersion  = 0;
InBuffDesc.cBuffers   = 1;
InBuffDesc.pBuffers   = &InSecBuff;
 
InSecBuff.cbBuffer    = cbIn;
InSecBuff.BufferType  = SECBUFFER_TOKEN;
InSecBuff.pvBuffer    = pIn;
 
ssStatus = g_pFuncs->AcceptSecurityContext (
                    &pAS->_hcred,
                    pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                    &InBuffDesc,
                    ASC_REQ_MUTUAL_AUTH,  // Context requirements.
                    SECURITY_NATIVE_DREP,
                    &pAS->_hctxt,
                    &OutBuffDesc,
                    &ContextAttributes,
                    &Lifetime
                    );
if (!SEC_SUCCESS (ssStatus))  
{
    fprintf (stderr, "AcceptSecurityContext failed: %u\n", ssStatus);
    return FALSE;
}
if (!(ContextAttributes && ASC_RET_MUTUAL_AUTH)) 
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete the authentication token, if necessary.
if ((SEC_I_COMPLETE_NEEDED == ssStatus) || 
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
 
return TRUE;
}
```



 

 