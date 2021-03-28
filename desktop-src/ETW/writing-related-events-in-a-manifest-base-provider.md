---
description: Use a função EventWriteTransfer quando vários componentes desejarem relacionar seus eventos em um cenário de rastreamento de ponta a ponta.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Gravando eventos relacionados em um provedor baseado em manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502065"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a><span data-ttu-id="f34f6-103">Gravando eventos relacionados em um provedor baseado em manifesto</span><span class="sxs-lookup"><span data-stu-id="f34f6-103">Writing Related Events in a Manifest-based Provider</span></span>

<span data-ttu-id="f34f6-104">Use a função [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) quando vários componentes desejarem relacionar seus eventos em um cenário de rastreamento de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="f34f6-104">Use the [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) function when several components want to relate their events in an end-to-end tracing scenario.</span></span> <span data-ttu-id="f34f6-105">Por exemplo, os componentes A, B e C executam trabalho em uma atividade relacionada e desejam vincular todos os eventos relacionados a essa atividade.</span><span class="sxs-lookup"><span data-stu-id="f34f6-105">For example, components A, B and C perform work on a related activity and want to link all the events related to that activity.</span></span>

<span data-ttu-id="f34f6-106">O ETW usa o armazenamento local de thread para tornar o identificador de atividade do componente anterior disponível para o próximo componente.</span><span class="sxs-lookup"><span data-stu-id="f34f6-106">ETW uses thread local storage to make the previous component's activity identifier available to the next component.</span></span> <span data-ttu-id="f34f6-107">O componente recupera o identificador do componente anterior do armazenamento local e define o identificador de atividade relacionado a ele.</span><span class="sxs-lookup"><span data-stu-id="f34f6-107">The component retrieves the previous component's identifier from the local storage and sets the related activity identifier to it.</span></span> <span data-ttu-id="f34f6-108">O consumidor pode usar o identificador de atividade relacionado para percorrer a cadeia dos eventos de um componente para o próximo.</span><span class="sxs-lookup"><span data-stu-id="f34f6-108">The consumer can then use the related activity identifier to walk the chain of the events from one component to the next.</span></span>

 

 



