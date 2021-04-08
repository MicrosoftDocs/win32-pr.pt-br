---
title: Interfaces NDF
description: As interfaces a seguir podem ser usadas para estender a funcionalidade das classes auxiliares da Microsoft que são identificadas como extensível.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004791"
---
# <a name="ndf-interfaces"></a><span data-ttu-id="9869b-103">Interfaces NDF</span><span class="sxs-lookup"><span data-stu-id="9869b-103">NDF Interfaces</span></span>

<span data-ttu-id="9869b-104">As interfaces a seguir podem ser usadas para estender a funcionalidade das classes auxiliares da Microsoft que são identificadas como extensível.</span><span class="sxs-lookup"><span data-stu-id="9869b-104">The following interfaces can be used to extend the functionality of Microsoft Helper Classes that are identified as extensible.</span></span> <span data-ttu-id="9869b-105">Embora essa funcionalidade não seja necessária para a maioria dos aplicativos, ela pode fornecer diagnósticos e resoluções mais específicos em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="9869b-105">Although this functionality is not required for most applications, it can provide more specific diagnoses and resolutions in some cases.</span></span>

> [!Note]  
> <span data-ttu-id="9869b-106">Essas interfaces e seus métodos associados são para desenvolvedores que implementam suas próprias classes auxiliares de terceiros que estendem a funcionalidade NDF.</span><span class="sxs-lookup"><span data-stu-id="9869b-106">These interfaces and their associated methods are for developers implementing their own third party helper classes that extend NDF functionality.</span></span>

 



| <span data-ttu-id="9869b-107">Nome da Interface</span><span class="sxs-lookup"><span data-stu-id="9869b-107">Interface Name</span></span>                                                 | <span data-ttu-id="9869b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9869b-108">Description</span></span>                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9869b-109">**INetDiagHelper**</span><span class="sxs-lookup"><span data-stu-id="9869b-109">**INetDiagHelper**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | <span data-ttu-id="9869b-110">Chamado pelo NDF para a maioria das atividades que ocorrem durante um diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="9869b-110">Called by the NDF for most activities that occur during a diagnosis.</span></span>                                                     |
| [<span data-ttu-id="9869b-111">**INetDiagHelperEx**</span><span class="sxs-lookup"><span data-stu-id="9869b-111">**INetDiagHelperEx**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | <span data-ttu-id="9869b-112">Chamado pelo NDF para capturar e fornecer informações associadas aos diagnósticos e à resolução de problemas relacionados à rede.</span><span class="sxs-lookup"><span data-stu-id="9869b-112">Called by the NDF to capture and provide information associated with diagnoses and resolution of network-related issues.</span></span> |
| [<span data-ttu-id="9869b-113">**INetDiagHelperInfo**</span><span class="sxs-lookup"><span data-stu-id="9869b-113">**INetDiagHelperInfo**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | <span data-ttu-id="9869b-114">Chamado pelo NDF para validar que ele tem as informações necessárias</span><span class="sxs-lookup"><span data-stu-id="9869b-114">Called by the NDF to validate that it has required information</span></span>                                                           |
| [<span data-ttu-id="9869b-115">**INetDiagHelperUtilFactory**</span><span class="sxs-lookup"><span data-stu-id="9869b-115">**INetDiagHelperUtilFactory**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | <span data-ttu-id="9869b-116">Reservado para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="9869b-116">Reserved for system use.</span></span>                                                                                                 |



 

 

 




