---
title: Propriedades da mensagem e da fila de mensagens
description: Uma mensagem tem propriedades, que especificam um rótulo, um corpo de mensagem e várias opções.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292427"
---
# <a name="message-and-message-queue-properties"></a><span data-ttu-id="75a0b-103">Propriedades da mensagem e da fila de mensagens</span><span class="sxs-lookup"><span data-stu-id="75a0b-103">Message and Message Queue Properties</span></span>

<span data-ttu-id="75a0b-104">Uma mensagem tem propriedades, que especificam um rótulo, um corpo de mensagem e várias opções.</span><span class="sxs-lookup"><span data-stu-id="75a0b-104">A message has properties, which specify a label, a message body, and a number of options.</span></span> <span data-ttu-id="75a0b-105">As opções de propriedade de mensagem podem incluir qualidade de serviço, prioridade, registro no diário, privacidade e níveis de autenticação e o tempo de vida da mensagem.</span><span class="sxs-lookup"><span data-stu-id="75a0b-105">Message property options can include quality of service, priority, journaling, privacy and authentication levels, and the lifetime of the message.</span></span> <span data-ttu-id="75a0b-106">Em aplicativos convencionais de enfileiramento de mensagens (não RPC), você especifica essas propriedades chamando as funções da API MSMQ ou os métodos de objeto COM, que são descritos na documentação do SDK do MSMQ.</span><span class="sxs-lookup"><span data-stu-id="75a0b-106">In conventional (non-RPC) message-queuing applications, you specify these properties by calling the MSMQ API functions or COM object methods, which are described in the MSMQ SDK documentation.</span></span> <span data-ttu-id="75a0b-107">Os aplicativos cliente RPC podem definir certas propriedades para chamadas de procedimento remoto chamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) e [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="75a0b-107">RPC client applications can set certain properties for remote procedure calls by calling [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) and [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span> <span data-ttu-id="75a0b-108">Uma vez definido, as propriedades permanecem em vigor para cada mensagem até que o aplicativo cliente as redefina.</span><span class="sxs-lookup"><span data-stu-id="75a0b-108">Once set, the properties remain in effect for each message until the client application resets them.</span></span>

<span data-ttu-id="75a0b-109">Uma fila de mensagens tem seu próprio conjunto de propriedades, além das mensagens.</span><span class="sxs-lookup"><span data-stu-id="75a0b-109">A message queue has its own set of properties, apart from those of the messages.</span></span> <span data-ttu-id="75a0b-110">Essas propriedades identificam exclusivamente uma fila e definem a classe de serviço que a fila fornece, os níveis de privacidade e autenticação necessários para as mensagens nessa fila e se as mensagens devem fazer parte de uma transação distribuída.</span><span class="sxs-lookup"><span data-stu-id="75a0b-110">These properties uniquely identify a queue and define the class of service that the queue provides, the privacy and authentication levels required for messages in this queue, and whether the messages are to be part of a distributed transaction.</span></span> <span data-ttu-id="75a0b-111">Assim como acontece com as propriedades de mensagem, você especifica as propriedades de uma fila de mensagens chamando as funções da API MSMQ ou os métodos de objeto COM, que são descritos na documentação do MSMQ.</span><span class="sxs-lookup"><span data-stu-id="75a0b-111">As with message properties, you specify the properties of a message queue by calling the MSMQ API functions or COM object methods, which are described in the MSMQ documentation.</span></span> <span data-ttu-id="75a0b-112">No entanto, um aplicativo de servidor RPC pode especificar propriedades de sua própria fila de recebimento quando chama [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) para estabelecer a associação.</span><span class="sxs-lookup"><span data-stu-id="75a0b-112">However, an RPC server application can specify properties of its own receive queue when it calls [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) to establish the binding.</span></span>

 

 




