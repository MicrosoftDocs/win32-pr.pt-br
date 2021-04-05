---
description: O exemplo a seguir mostra uma mensagem que está sendo criptografada antes de ser enviada para um computador remoto pela conexão segura.
ms.assetid: 1788b496-ad19-427e-be07-4aa68543fced
title: Criptografando uma mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fcc987e17c37f9b2eb80289f257101b51f5f3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826821"
---
# <a name="encrypting-a-message"></a><span data-ttu-id="d79b8-103">Criptografando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="d79b8-103">Encrypting a Message</span></span>

<span data-ttu-id="d79b8-104">O exemplo a seguir mostra uma mensagem que está sendo criptografada antes de ser enviada para um computador remoto pela conexão segura.</span><span class="sxs-lookup"><span data-stu-id="d79b8-104">The following example shows a message being encrypted before it is sent to a remote computer over the secure connection.</span></span>

<span data-ttu-id="d79b8-105">O exemplo supõe que uma variável **SecHandle** chamada `phContext` e um **soquete** nomeado `s` sejam inicializados.</span><span class="sxs-lookup"><span data-stu-id="d79b8-105">The example assumes that a **SecHandle** variable named `phContext` and a **SOCKET** named `s` are initialized.</span></span> <span data-ttu-id="d79b8-106">Para as declarações e as iniciações dessas variáveis, consulte [usando o SSPI com um cliente do Windows Sockets](using-sspi-with-a-windows-sockets-client.md) e [usando o SSPI com um servidor do Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="d79b8-106">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="d79b8-107">Este exemplo inclui chamadas para funções em Secur32. lib, que devem ser incluídas entre as bibliotecas de link.</span><span class="sxs-lookup"><span data-stu-id="d79b8-107">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_StreamSizes  Sizes;
SECURITY_STATUS            scRet;
SecBufferDesc              Message;
SecBuffer                  Buffers[4];
SecBuffer                  *pDataBuffer;

PBYTE                       pbIoBuffer;
DWORD                       cbIoBuffer;
DWORD                       cbIoBufferLength;
PBYTE                       pbMessage;
DWORD                       cbMessage;

//--------------------------------------------------------------------
// Get the stream encryption sizes. This needs to 
// be done once per connection. 
// phContext must have been initialized during the handshake process.

scRet = QueryContextAttributes(
            phContext,
            SECPKG_ATTR_STREAM_SIZES,
            &Sizes);

if(FAILED(scRet))
{
    MyHandleError("Error reading SECPKG_ATTR_STREAM_SIZES");
}

//--------------------------------------------------------------------
// Allocate a working buffer. The plaintext sent to EncryptMessage
// can never be more than 'Sizes.cbMaximumMessage', so a buffer 
// size of Sizes.cbMaximumMessage plus the header and trailer sizes 
// is sufficient for the longest message.

cbIoBufferLength = Sizes.cbHeader + 
                   Sizes.cbMaximumMessage +
                   Sizes.cbTrailer;

if(!(pbIoBuffer = malloc((BYTE *), cbIoBufferLength)))
{
    MyHandleError("Out of memory");
}

//--------------------------------------------------------------------
// Create a plaintext message to be encrypted offset into the data 
// buffer by "header size" bytes. This allows encryption in place.

pbMessage = pbIoBuffer + Sizes.cbHeader;

StringCbPrintfA(pbMessage,
                cbIoBufferLength - Sizes.cbHeader,
                "This is the plaintext message.");
cbMessage = strlen(pbMessage);

//--------------------------------------------------------------------
// Encrypt the plaintext message.

Buffers[0].pvBuffer     = pbIoBuffer;
Buffers[0].cbBuffer     = Sizes.cbHeader;
Buffers[0].BufferType   = SECBUFFER_STREAM_HEADER;

Buffers[1].pvBuffer     = pbMessage;
Buffers[1].cbBuffer     = cbMessage;
Buffers[1].BufferType   = SECBUFFER_DATA;

Buffers[2].pvBuffer     = pbMessage + cbMessage;
Buffers[2].cbBuffer     = Sizes.cbTrailer;
Buffers[2].BufferType   = SECBUFFER_STREAM_TRAILER;

Buffers[3].BufferType   = SECBUFFER_EMPTY;

Message.ulVersion       = SECBUFFER_VERSION;
Message.cBuffers        = 4;
Message.pBuffers        = Buffers;

scRet = EncryptMessage(phContext, 0, &Message, 0);

if(FAILED(scRet))
{
    MyHandleError("Error returned by EncryptMessage.");
}

//--------------------------------------------------------------------
// Send the encrypted data.

if(!(SendMsg(
     s,
     pbIoBuffer,
     Buffers[0].cbBuffer + Buffers[1].cbBuffer + 
           Buffers[2].cbBuffer)))
{
     MyHandleError("SendMsg failed.");
}
```



 

 



