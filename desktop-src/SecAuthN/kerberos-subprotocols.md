---
description: O protocolo Kerberos é composto por três subprotocolos.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Subprotocolos Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169829"
---
# <a name="kerberos-subprotocols"></a><span data-ttu-id="c1fcf-103">Subprotocolos Kerberos</span><span class="sxs-lookup"><span data-stu-id="c1fcf-103">Kerberos Subprotocols</span></span>

<span data-ttu-id="c1fcf-104">O [*protocolo Kerberos*](../secgloss/k-gly.md) é composto por três subprotocolos.</span><span class="sxs-lookup"><span data-stu-id="c1fcf-104">The [*Kerberos protocol*](../secgloss/k-gly.md) is composed of three subprotocols.</span></span>



| <span data-ttu-id="c1fcf-105">Subprotocolo</span><span class="sxs-lookup"><span data-stu-id="c1fcf-105">Subprotocol</span></span>                                                                         | <span data-ttu-id="c1fcf-106">Significado</span><span class="sxs-lookup"><span data-stu-id="c1fcf-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1fcf-107">Troca de serviços de autenticação</span><span class="sxs-lookup"><span data-stu-id="c1fcf-107">Authentication Service Exchange</span></span>](authentication-service-exchange.md)<br/>   | <span data-ttu-id="c1fcf-108">Nesse subprotocolo, o [*centro de distribuição de chaves*](../secgloss/k-gly.md) (KDC) fornece ao cliente uma chave de [*sessão*](../secgloss/s-gly.md) de logon e um tíquete de concessão de tíquete (TGT).</span><span class="sxs-lookup"><span data-stu-id="c1fcf-108">In this subprotocol, the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) gives the client a logon [*session key*](../secgloss/s-gly.md) and a ticket-granting ticket (TGT).</span></span><br/> |
| [<span data-ttu-id="c1fcf-109">Troca de serviços de concessão de tíquete</span><span class="sxs-lookup"><span data-stu-id="c1fcf-109">Ticket-Granting Service Exchange</span></span>](ticket-granting-service-exchange.md)<br/> | <span data-ttu-id="c1fcf-110">Nesse subprotocolo, o KDC distribui uma chave de sessão de serviço e um tíquete para o serviço.</span><span class="sxs-lookup"><span data-stu-id="c1fcf-110">In this subprotocol, the KDC distributes a service session key and a ticket for the service.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="c1fcf-111">Troca de cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="c1fcf-111">Client/Server Exchange</span></span>](client-server-exchange.md)<br/>                     | <span data-ttu-id="c1fcf-112">Nesse subprotocolo, o cliente apresenta o tíquete para a admissão a um serviço.</span><span class="sxs-lookup"><span data-stu-id="c1fcf-112">In this subprotocol, the client presents the ticket for admission to a service.</span></span><br/>                                                                                                                                                                                                                         |



 

 

 
