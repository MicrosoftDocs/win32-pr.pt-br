---
description: Quando um cliente e um servidor concluem a configuração do contexto de segurança, as funções de suporte a mensagens podem ser usadas.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Assinando uma mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f8151a66120575bfcaeda62955a7f6aa47e8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749222"
---
# <a name="signing-a-message"></a><span data-ttu-id="69c22-103">Assinando uma mensagem</span><span class="sxs-lookup"><span data-stu-id="69c22-103">Signing a Message</span></span>

<span data-ttu-id="69c22-104">Quando um cliente e um servidor concluem a configuração do [*contexto de segurança*](../secgloss/s-gly.md), as funções de suporte a mensagens podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="69c22-104">When a client and server finish setting up the [*security context*](../secgloss/s-gly.md), message support functions can be used.</span></span> <span data-ttu-id="69c22-105">O cliente e o servidor usam o token de contexto de segurança criado quando a sessão foi estabelecida para chamar as funções [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="69c22-105">The client and server use the security context token created when the session was established to call [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions.</span></span> <span data-ttu-id="69c22-106">O token de contexto pode ser usado com [**EncryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (geral)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para [*privacidade*](../secgloss/p-gly.md)de comunicação.</span><span class="sxs-lookup"><span data-stu-id="69c22-106">The context token can be used with [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) for communications [*privacy*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="69c22-107">O exemplo a seguir mostra o lado do cliente que gera uma mensagem assinada para enviar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="69c22-107">The following example shows the client side generating a signed message to send to the server.</span></span> <span data-ttu-id="69c22-108">Antes de chamar [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), o cliente chama [**QueryContextAttributes (geral)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) com uma estrutura de [**\_ tamanhos SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) para determinar o tamanho do buffer necessário para manter a assinatura da mensagem.</span><span class="sxs-lookup"><span data-stu-id="69c22-108">Before calling [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), the client calls [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) with a [**SecPkgContext\_Sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) structure to determine the length of the buffer needed to hold the message signature.</span></span> <span data-ttu-id="69c22-109">Se o membro **cbMaxSignature** for zero, o [*pacote de segurança*](../secgloss/s-gly.md) não oferecerá suporte a mensagens de assinatura.</span><span class="sxs-lookup"><span data-stu-id="69c22-109">If the **cbMaxSignature** member is zero, the [*security package*](../secgloss/s-gly.md) does not support signing messages.</span></span> <span data-ttu-id="69c22-110">Caso contrário, esse membro indica o tamanho do buffer a ser alocado para receber a assinatura.</span><span class="sxs-lookup"><span data-stu-id="69c22-110">Otherwise, this member indicates the size of the buffer to allocate to receive the signature.</span></span>

<span data-ttu-id="69c22-111">O exemplo supõe que uma variável **SecHandle** chamada *phContext* e uma estrutura de **soquete** chamada *s* são inicializadas.</span><span class="sxs-lookup"><span data-stu-id="69c22-111">The example assumes that a **SecHandle** variable named *phContext* and a **SOCKET** structure named *s* are initialized.</span></span> <span data-ttu-id="69c22-112">Para as declarações e as iniciações dessas variáveis, consulte [usando o SSPI com um cliente do Windows Sockets](using-sspi-with-a-windows-sockets-client.md) e [usando o SSPI com um servidor do Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="69c22-112">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="69c22-113">Este exemplo inclui chamadas para funções em Secur32. lib, que devem ser incluídas entre as bibliotecas de link.</span><span class="sxs-lookup"><span data-stu-id="69c22-113">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


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



<span data-ttu-id="69c22-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) retornará **true** se o contexto for configurado para permitir mensagens de assinatura e se o descritor de buffer de entrada estiver formatado corretamente.</span><span class="sxs-lookup"><span data-stu-id="69c22-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) returns **TRUE** if the context is set up to allow signing messages and if the input buffer descriptor is correctly formatted.</span></span> <span data-ttu-id="69c22-115">Depois que a mensagem é assinada, a mensagem e a assinatura com seus comprimentos são enviadas para o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="69c22-115">After the message is signed, the message and the signature with their lengths are sent to the remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="69c22-116">O conteúdo dos dados das estruturas [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) são enviados, não as estruturas **SecBuffer** nem a estrutura [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="69c22-116">The data contents of the [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures are sent, not the **SecBuffer** structures themselves nor the [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="69c22-117">Novas estruturas **SecBuffer** e uma nova estrutura **SecBufferDesc** são criadas pelo aplicativo de recebimento para verificar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="69c22-117">New **SecBuffer** structures and a new **SecBufferDesc** structure are created by the receiving application to verify the signature.</span></span>

 

 

 
