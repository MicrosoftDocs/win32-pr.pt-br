---
title: O que há de novo nas APIs UPnP
description: As APIs de™ UPnP têm novos recursos e a documentação atualizada do Windows XP SP2. A tabela a seguir identifica a nova documentação.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637185"
---
# <a name="whats-new-in-the-upnp-apis"></a><span data-ttu-id="ab385-104">O que há de novo nas APIs UPnP</span><span class="sxs-lookup"><span data-stu-id="ab385-104">What's New in the UPnP APIs</span></span>

<span data-ttu-id="ab385-105">As APIs de™ UPnP têm novos recursos e a documentação atualizada do Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="ab385-105">The UPnP™ APIs have new features and updated documentation for Windows XP SP2.</span></span> <span data-ttu-id="ab385-106">A tabela a seguir identifica a nova documentação.</span><span class="sxs-lookup"><span data-stu-id="ab385-106">The following table identifies the new documentation.</span></span>



| <span data-ttu-id="ab385-107">Recurso</span><span class="sxs-lookup"><span data-stu-id="ab385-107">Feature</span></span>                                                          | <span data-ttu-id="ab385-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab385-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab385-109">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="ab385-109">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | <span data-ttu-id="ab385-110">Essa nova interface permite que um dispositivo hospedado Obtenha informações sobre um solicitante (isto é, um ponto de controle) e a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ab385-110">This new interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.</span></span> <span data-ttu-id="ab385-111">Ele inclui três métodos, cada um dos quais fornece um tipo diferente de informações.</span><span class="sxs-lookup"><span data-stu-id="ab385-111">It includes three methods, each of which provides a different type of information.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="ab385-112">Implementando o comportamento do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ab385-112">Implementing Device Behavior</span></span>](implementing-device-behavior.md) | <span data-ttu-id="ab385-113">Este tópico inclui uma nova seção que explica como obter informações de ponto de extremidade usando a nova interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .</span><span class="sxs-lookup"><span data-stu-id="ab385-113">This topic includes a new section that explains how to obtain endpoint information by using the new [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) interface.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="ab385-114">Definições de configuração</span><span class="sxs-lookup"><span data-stu-id="ab385-114">Configuration Settings</span></span>](configuration-settings.md)             | <span data-ttu-id="ab385-115">Este novo tópico fornece informações sobre as configurações do registro que afetam o comportamento das APIs de UPnP.</span><span class="sxs-lookup"><span data-stu-id="ab385-115">This new topic provides information about the registry settings that affect the behavior of the UPnP APIs.</span></span>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="ab385-116">Códigos de erro do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ab385-116">Device Error Codes</span></span>](device-error-codes.md)                     | <span data-ttu-id="ab385-117">Este novo tópico explica como um código de erro de um dispositivo é convertido em um valor HRESULT e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="ab385-117">This new topic explains how an error code from a device is converted to an HRESULT value and vice versa.</span></span> <span data-ttu-id="ab385-118">Uma compreensão desse processo é necessária para avaliar um valor HRESULT que é retornado pelos métodos [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**IUPnPService:: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) .</span><span class="sxs-lookup"><span data-stu-id="ab385-118">An understanding of this process is necessary in order to evaluate an HRESULT value that is returned by the [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) and [**IUPnPService::QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) methods.</span></span> |



 

 

 




