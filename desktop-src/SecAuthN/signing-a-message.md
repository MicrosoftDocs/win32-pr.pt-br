---
description: Quando um cliente e um servidor concluem a configuração do contexto de segurança, as funções de suporte a mensagens podem ser usadas.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Assinando uma mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b605ccaaa4adfe37dc2bbe5f5c0ed809f0656896e5e85478b0b63740bf6f63e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918045"
---
# <a name="signing-a-message"></a>Assinando uma mensagem

Quando um cliente e um servidor concluem a configuração do [*contexto de segurança*](../secgloss/s-gly.md), as funções de suporte a mensagens podem ser usadas. O cliente e o servidor usam o token de contexto de segurança criado quando a sessão foi estabelecida para chamar as funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) . O token de contexto pode ser usado com [**EncryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para [*privacidade*](../secgloss/p-gly.md)de comunicação.

O exemplo a seguir mostra o lado do cliente que gera uma mensagem assinada para enviar ao servidor. Antes de chamar [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), o cliente chama [**QueryContextAttributes (geral)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) com uma estrutura de [**\_ tamanhos SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) para determinar o tamanho do buffer necessário para manter a assinatura da mensagem. Se o membro **cbMaxSignature** for zero, o [*pacote de segurança*](../secgloss/s-gly.md) não oferecerá suporte a mensagens de assinatura. Caso contrário, esse membro indica o tamanho do buffer a ser alocado para receber a assinatura.

O exemplo supõe que uma variável **SecHandle** chamada *phContext* e uma estrutura de **soquete** chamada *s* são inicializadas. para as declarações e as iniciações dessas variáveis, consulte [usando sspi com um cliente de soquetes Windows](using-sspi-with-a-windows-sockets-client.md) e [usando sspi com um servidor de soquetes de Windows](using-sspi-with-a-windows-sockets-server.md). Este exemplo inclui chamadas para funções em Secur32. lib, que devem ser incluídas entre as bibliotecas de link.


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_Sizes ContextSizes;
char *MessageBuffer = "This is a sample buffer to be signed.";
DWORD MessageBufferSize = strlen(MessageBuffer);
SecBufferDesc InputBufferDescriptor;
SecBuffer InputSecurityToken[2];

ss = QueryContextAttributes(
    &phContext,
    SECPKG_ATTR_SIZES,
    &ContextSizes
    );
if(ContextSizes.cbMaxSignature == 0)
{
     MyHandleError("This session does not support message signing.");
}
//--------------------------------------------------------------------
// The message as a byte string is in the variable 
// MessageBuffer, and its length is in MessageBufferSize. 

//--------------------------------------------------------------------
// Build the buffer descriptor and the buffers 
// to pass to the MakeSignature call.

InputBufferDescriptor.cBuffers = 2;
InputBufferDescriptor.pBuffers = InputSecurityToken;
InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

//--------------------------------------------------------------------
// Build a security buffer for the message itself. If 
// the SECBUFFER_READONLY attribute is set, the buffer will not be
// signed.

InputSecurityToken[0].BufferType = SECBUFFER_DATA;
InputSecurityToken[0].cbBuffer = MessageBufferSize;
InputSecurityToken[0].pvBuffer = MessageBuffer;

//--------------------------------------------------------------------
// Allocate and build a security buffer for the message
// signature.

InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
InputSecurityToken[1].cbBuffer = ContextSizes.cbMaxSignature;
InputSecurityToken[1].pvBuffer = 
        (void *)malloc(ContextSizes.cbMaxSignature);

//--------------------------------------------------------------------
// Call MakeSignature 
// For the NTLM package, the sequence number need not be specified 
// because the package provides sequencing.
// The quality of service parameter is ignored.

Ss = MakeSignature(
    &phContext,
    0,                       // no quality of service
    &InputBufferDescriptor,  // input message descriptor
    0                        // no sequence number
    );
if (SEC_SUCCESS(ss))
{
     printf("Have made a signature.\n");
}
else
{ 
    MyHandleError("MakeSignature Failed."); 
}

//--------------------------------------------------------------------
//  Send the message.

if(!SendMsg(
    s,
    (BYTE *)InputSecurityToken[0].pvBuffer,
    InputSecurityToken[0].cbBuffer))
{
     MyHandleError("The message was not sent.");
}

//--------------------------------------------------------------------
//   Send the signature.

if(!SendMsg(
     s,
    (BYTE *)InputSecurityToken[1].pvBuffer,
    InputSecurityToken[1].cbBuffer ))
{
     MyHandleError("The signature was not sent.");
}
```



[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) retornará **true** se o contexto for configurado para permitir mensagens de assinatura e se o descritor de buffer de entrada estiver formatado corretamente. Depois que a mensagem é assinada, a mensagem e a assinatura com seus comprimentos são enviadas para o computador remoto.

> [!Note]  
> O conteúdo dos dados das estruturas [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) são enviados, não as estruturas **SecBuffer** nem a estrutura [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) . Novas estruturas **SecBuffer** e uma nova estrutura **SecBufferDesc** são criadas pelo aplicativo de recebimento para verificar a assinatura.

 

 

 
