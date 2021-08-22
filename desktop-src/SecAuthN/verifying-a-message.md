---
description: O exemplo a seguir mostra o código para receber e verificar uma mensagem assinada. O exemplo recebe o buffer de assinatura e seu tamanho em SignatureBuffer e SignatureBufferSize e o buffer de mensagens e seu tamanho em MessageBuffer e MessageBufferSize.
ms.assetid: 3e71aa0f-d135-4311-96f3-305762543627
title: Verificando uma mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90850a88ede875ae41549bca79aceb2d7bdea17db6f50eeb1a3a5e6dfb9a921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915085"
---
# <a name="verifying-a-message"></a>Verificando uma mensagem

O exemplo a seguir mostra o código para receber e verificar uma mensagem assinada. O exemplo recebe o buffer de assinatura e seu tamanho em SignatureBuffer e SignatureBufferSize e o buffer de mensagens e seu tamanho em MessageBuffer e MessageBufferSize.

O exemplo supõe que uma variável **SecHandle** chamada phContext e uma estrutura de **soquete** chamada s são inicializadas. para as declarações e as iniciações dessas variáveis, consulte [usando sspi com um cliente de soquetes Windows](using-sspi-with-a-windows-sockets-client.md) e [usando sspi com um servidor de soquetes de Windows](using-sspi-with-a-windows-sockets-server.md). Esse código inclui chamadas para funções em Secur32. lib, que devem ser incluídas entre as bibliotecas de links.


```C++
//--------------------------------------------------------------------
//  Declare and initialize local variables.
#include <windows.h>
#include <stdio.h>
#include <sspi.h>

#define SECURITY_WIN32
#define MaxMessageLength 1024
#define BUFSIZ 512

void main()
{
    BYTE MessageBuffer[BUFSIZ];
    BYTE SignatureBuffer[BUFSIZ];
    DWORD MessageBufferSize;
    DWORD SignatureBufferSize;
    SECURITY_STATUS SecStatus;
    SecBufferDesc InputBufferDescriptor;
    SecBuffer InputSecurityToken[2];
    ULONG fQOP;

    //------------------------------------------------------------------
    //    Receive the message.

    if(!(ReceiveMsg(
         s,
         MessageBuffer,
         MaxMessageLength,
         &MessageBufferSize)))
    {
         MyHandleError("Error. Message not received.");
    }

    //------------------------------------------------------------------
    //    Receive the signature.

    if(!(ReceiveMsg(
         s,
         SignatureBuffer,
         MaxMessageLength,
         &SignatureBufferSize)))
    {
         MyHandleError("Error. Signature not received.");
    }

    //------------------------------------------------------------------
    // Build the input buffer descriptor.

    InputBufferDescriptor.cBuffers = 2;
    InputBufferDescriptor.pBuffers = InputSecurityToken;
    InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

    //-------------------------------------------------------------------
    // Build the security buffer for the message.

    InputSecurityToken[0].BufferType = SECBUFFER_DATA;
    InputSecurityToken[0].cbBuffer = MessageBufferSize;
    InputSecurityToken[0].pvBuffer = MessageBuffer;

    //-------------------------------------------------------------------
    // Build the security buffer for the signature.

    InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
    InputSecurityToken[1].cbBuffer = SignatureBufferSize;
    InputSecurityToken[1].pvBuffer = SignatureBuffer;

    //--------------------------------------------------------------------
    // Call VerifySignature. 

    SecStatus = VerifySignature(
          &phContext,
          &InputBufferDescriptor,  // input message descriptor
          0,                       // no sequence number
          &fQOP                    // quality of protection
          );
    if(SecStatus == SEC_E_OK)
    {
         printf("The signature verified the message.\n");
    }
    else
         if(SecStatus == SEC_E_MESSAGE_ALTERED)
         {
              printf("The message was altered in transit.\n");
         }
         else
              if(SecStatus == SEC_E_OUT_OF_SEQUENCE )
              {
                  printf("The message is out of sequence.\n");
              }
              else
              {
                  printf("An unknown error occurred in VerifyMessage.\n");
              }
}
```



 

 



