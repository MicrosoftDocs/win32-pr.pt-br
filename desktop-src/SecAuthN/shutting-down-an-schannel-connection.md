---
description: Desligando uma conexão Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Desligando uma conexão Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646675"
---
# <a name="shutting-down-an-schannel-connection"></a><span data-ttu-id="8addb-103">Desligando uma conexão Schannel</span><span class="sxs-lookup"><span data-stu-id="8addb-103">Shutting Down an Schannel Connection</span></span>

<span data-ttu-id="8addb-104">Quando um cliente ou servidor é concluído com uma conexão, ele deve desligá-lo.</span><span class="sxs-lookup"><span data-stu-id="8addb-104">When a client or server is finished with a connection, it must shut it down.</span></span> <span data-ttu-id="8addb-105">A outra parte, por sua vez, deve reconhecer o desligamento e excluir a conexão.</span><span class="sxs-lookup"><span data-stu-id="8addb-105">The other party, in turn, must recognize the shutdown and delete the connection.</span></span>

<span data-ttu-id="8addb-106">**Para desligar uma conexão Schannel**</span><span class="sxs-lookup"><span data-stu-id="8addb-106">**To shut down an Schannel connection**</span></span>

1.  <span data-ttu-id="8addb-107">Chame a função [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , especificando o \_ token de controle de desligamento Schannel.</span><span class="sxs-lookup"><span data-stu-id="8addb-107">Call the [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) function, specifying the SCHANNEL\_SHUTDOWN control token.</span></span>
2.  <span data-ttu-id="8addb-108">Depois de receber um \_ \_ valor de retorno de s E OK de [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), chame a função [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clientes) ou [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servidores), passando buffers vazios.</span><span class="sxs-lookup"><span data-stu-id="8addb-108">After receiving an SEC\_E\_OK return value from [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), call the [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) or [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servers) function, passing in empty buffers.</span></span>
3.  <span data-ttu-id="8addb-109">Prossiga como se o aplicativo estivesse criando uma nova conexão até que a função retorne o contexto de s \_ I, \_ \_ expirado ou s \_ e \_ OK, para indicar que a conexão foi desligada.</span><span class="sxs-lookup"><span data-stu-id="8addb-109">Proceed as though your application were creating a new connection until the function returns SEC\_I\_CONTEXT\_EXPIRED or SEC\_E\_OK to indicate that the connection is shut down.</span></span>
4.  <span data-ttu-id="8addb-110">Envie as informações de saída final, se houver, para a parte remota.</span><span class="sxs-lookup"><span data-stu-id="8addb-110">Send the final output information, if any, to the remote party.</span></span>
5.  <span data-ttu-id="8addb-111">Chame [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para liberar recursos mantidos pela conexão.</span><span class="sxs-lookup"><span data-stu-id="8addb-111">Call [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) to free resources held by the connection.</span></span>

## <a name="recognizing-a-shutdown"></a><span data-ttu-id="8addb-112">Reconhecendo um desligamento</span><span class="sxs-lookup"><span data-stu-id="8addb-112">Recognizing a Shutdown</span></span>

<span data-ttu-id="8addb-113">A função [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) retorna um \_ \_ contexto de s I \_ expirou quando o remetente da mensagem desligou a conexão.</span><span class="sxs-lookup"><span data-stu-id="8addb-113">The [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) function returns SEC\_I\_CONTEXT\_EXPIRED when the message sender has shut down the connection.</span></span> <span data-ttu-id="8addb-114">Depois de receber esse valor de retorno, siga o procedimento para desligar uma conexão Schannel, anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="8addb-114">After receiving this return value, follow the procedure To shut down an Schannel connection, earlier in this topic.</span></span>

 

 
