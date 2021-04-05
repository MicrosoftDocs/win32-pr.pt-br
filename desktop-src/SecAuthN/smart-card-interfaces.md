---
description: Uma interface de cartão inteligente consiste em um conjunto predefinido de serviços disponíveis em um cartão inteligente, os protocolos necessários para invocar os serviços e as suposições referentes ao contexto dos serviços.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfaces de cartão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662785"
---
# <a name="smart-card-interfaces"></a><span data-ttu-id="dc904-103">Interfaces de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="dc904-103">Smart Card Interfaces</span></span>

<span data-ttu-id="dc904-104">Uma interface de [*cartão inteligente*](../secgloss/s-gly.md) consiste em um conjunto predefinido de serviços disponíveis em um *cartão inteligente*, os protocolos necessários para invocar os serviços e as suposições referentes ao contexto dos serviços.</span><span class="sxs-lookup"><span data-stu-id="dc904-104">A [*smart card*](../secgloss/s-gly.md) interface consists of a predefined set of services available within a *smart card*, the protocols necessary to invoke the services, and any assumptions regarding the context of the services.</span></span>

<span data-ttu-id="dc904-105">Em relação a cartões inteligentes, o termo "interface" é semelhante a como ele é usado em COM, que, por sua vez, é semelhante em conceito ao identificador de aplicativo ISO 7816/5, mas com um escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="dc904-105">With respect to smart cards, the term "interface" is similar to how it is used in COM, which in turn is similar in concept to the ISO 7816/5 application identifier but with a different scope.</span></span>

<span data-ttu-id="dc904-106">Cada interface de cartão inteligente é identificada por um GUID.</span><span class="sxs-lookup"><span data-stu-id="dc904-106">Each smart card interface is identified by a GUID.</span></span> <span data-ttu-id="dc904-107">Por exemplo, uma interface pode ser definida que fornece informações de Biorhythm para seu detentor.</span><span class="sxs-lookup"><span data-stu-id="dc904-107">For example, an interface might be defined that provides biorhythm information to its holder.</span></span> <span data-ttu-id="dc904-108">Se um determinado cartão inteligente der suporte a esse serviço, ele poderá reivindicar suporte a esse GUID de interface.</span><span class="sxs-lookup"><span data-stu-id="dc904-108">If a given smart card supports this service, then it may claim to support that interface GUID.</span></span> <span data-ttu-id="dc904-109">Usando os GUIDs de interface, um aplicativo pode pesquisar um determinado conjunto de interfaces, localizando qualquer cartão que dê suporte a esse conjunto, para concluir uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="dc904-109">Using the interface GUIDs, an application may search for a particular set of interfaces, locating any card that supports that set, to complete a task.</span></span>

<span data-ttu-id="dc904-110">Embora uma interface tenha um GUID, ela pode ser implementada de forma diferente em cartões diferentes.</span><span class="sxs-lookup"><span data-stu-id="dc904-110">Although an interface has one GUID, it might be implemented differently on different cards.</span></span> <span data-ttu-id="dc904-111">Por exemplo, a interface Biorhythm mencionada acima pode ter várias implementações diferentes, mas todas são referenciadas usando o mesmo GUID.</span><span class="sxs-lookup"><span data-stu-id="dc904-111">For example, the biorhythm interface mentioned above can have several different implementations, yet all are referenced using the same GUID.</span></span> <span data-ttu-id="dc904-112">As diferentes implementações não alterariam a interação entre o aplicativo e o cartão inteligente; no entanto, a interação entre o [*provedor de serviços*](../secgloss/c-gly.md) e os cartões inteligentes pode diferir dependendo da implementação da interface.</span><span class="sxs-lookup"><span data-stu-id="dc904-112">The different implementations would not change the interaction between the application and the smart card; however, the interaction between the [*service provider*](../secgloss/c-gly.md) and the smart cards may differ depending on the interface's implementation.</span></span>

<span data-ttu-id="dc904-113">O conjunto de interfaces com suporte de um cartão inteligente é definido durante a introdução do cartão inteligente (consulte [apresentando cartões inteligentes ao sistema](introducing-smart-cards-to-the-system.md)).</span><span class="sxs-lookup"><span data-stu-id="dc904-113">The set of interfaces supported by a smart card is defined during smart card introduction (see [Introducing Smart Cards to the System](introducing-smart-cards-to-the-system.md)).</span></span>

 

 
