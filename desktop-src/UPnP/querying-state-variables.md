---
title: Consultando variáveis de estado
description: A interface IUPnPService fornece o método QueryStateVariable, que retorna o valor de uma variável de estado especificada.
ms.assetid: 9e8b98b0-488a-4f9c-9ad7-039dbd470486
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a716bbe93c2306eca43b977a42f33a85187f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292087"
---
# <a name="querying-state-variables"></a><span data-ttu-id="73515-103">Consultando variáveis de estado</span><span class="sxs-lookup"><span data-stu-id="73515-103">Querying State Variables</span></span>

<span data-ttu-id="73515-104">A interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) fornece o método [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) , que retorna o valor de uma variável de estado especificada.</span><span class="sxs-lookup"><span data-stu-id="73515-104">The [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface provides the [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) method, that returns the value of a specified state variable.</span></span>

<span data-ttu-id="73515-105">O fórum UPnP não incentiva o uso de [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span><span class="sxs-lookup"><span data-stu-id="73515-105">The UPnP Forum discourages the use of [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable).</span></span> <span data-ttu-id="73515-106">Os gravadores de dispositivos foram incentivados a escrever as ações apropriadas para fornecer essas informações.</span><span class="sxs-lookup"><span data-stu-id="73515-106">Device writers have been encouraged to write appropriate actions to provide this information.</span></span> <span data-ttu-id="73515-107">Os gravadores de dispositivo não têm obrigação de implementar **QueryStateVariable**.</span><span class="sxs-lookup"><span data-stu-id="73515-107">Device writers are under no obligation to implement **QueryStateVariable**.</span></span>

<span data-ttu-id="73515-108">Consulte a seção [chamando ações](invoking-actions.md).</span><span class="sxs-lookup"><span data-stu-id="73515-108">See the section [Invoking Actions](invoking-actions.md).</span></span>

 

 




