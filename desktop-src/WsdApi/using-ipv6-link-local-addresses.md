---
description: O endereçamento de link local IPv6 em mensagens SOAP fornece um desafio exclusivo, pois os endereços de link local IPv6 exigem uma ID de escopo significativa, mas a ID do escopo tem significado apenas para o computador local.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Usando endereços de link local IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89356042e8a71b0af19337b7013b8abd1e8a354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090991"
---
# <a name="using-ipv6-link-local-addresses"></a><span data-ttu-id="e6396-103">Usando endereços de link local IPv6</span><span class="sxs-lookup"><span data-stu-id="e6396-103">Using IPv6 Link-Local Addresses</span></span>

<span data-ttu-id="e6396-104">O endereçamento de link local IPv6 em mensagens SOAP fornece um desafio exclusivo, pois os endereços de link local IPv6 exigem uma ID de escopo significativa, mas a ID do escopo tem significado apenas para o computador local.</span><span class="sxs-lookup"><span data-stu-id="e6396-104">IPv6 link-local addressing in SOAP messages provides a unique challenge, as IPv6 link-local addresses require a scope ID to be meaningful, but the scope ID only has meaning for the local machine.</span></span> <span data-ttu-id="e6396-105">Todas as implementações de cliente e dispositivo devem remover a ID de escopo antes de enviar um endereço de link local IPv6 em uma mensagem SOAP.</span><span class="sxs-lookup"><span data-stu-id="e6396-105">All client and device implementations must remove the scope ID before sending an IPv6 link-local address in a SOAP message.</span></span> <span data-ttu-id="e6396-106">Além disso, quando um endereço de link local IPv6 é recebido em uma mensagem, a interface em que a mensagem foi recebida deve ser conhecida para que o endereço local do link completo com a ID de escopo possa ser reconstruído.</span><span class="sxs-lookup"><span data-stu-id="e6396-106">Additionally, when an IPv6 link-local address is received in a message, the interface the message was received on must be known so the complete link local address with scope ID can be reconstructed.</span></span>

 

 



