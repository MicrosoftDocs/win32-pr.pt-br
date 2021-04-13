---
description: A interface IUpdateSearcher define as propriedades a seguir.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Propriedades de IUpdateSearcher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/11/2021
ms.locfileid: "104298452"
---
# <a name="iupdatesearcher-properties"></a><span data-ttu-id="15762-103">Propriedades de IUpdateSearcher</span><span class="sxs-lookup"><span data-stu-id="15762-103">IUpdateSearcher Properties</span></span>

<span data-ttu-id="15762-104">A interface [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="15762-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following properties.</span></span>



| <span data-ttu-id="15762-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="15762-105">Property</span></span>                                                                                           | <span data-ttu-id="15762-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="15762-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15762-107">**CanAutomaticallyUpgradeService**</span><span class="sxs-lookup"><span data-stu-id="15762-107">**CanAutomaticallyUpgradeService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | <span data-ttu-id="15762-108">Obtém e define um valor booliano que indica se chamadas futuras para os métodos [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) e [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) resultam em uma atualização automática para o WUA (Windows Update Agent).</span><span class="sxs-lookup"><span data-stu-id="15762-108">Gets and sets a Boolean value that indicates whether future calls to the [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) and [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) methods result in an automatic upgrade to Windows Update Agent (WUA).</span></span> |
| [<span data-ttu-id="15762-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="15762-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | <span data-ttu-id="15762-110">Identifica o aplicativo cliente atual.</span><span class="sxs-lookup"><span data-stu-id="15762-110">Identifies the current client application.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="15762-111">**IncludePotentiallySupersededUpdates**</span><span class="sxs-lookup"><span data-stu-id="15762-111">**IncludePotentiallySupersededUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | <span data-ttu-id="15762-112">Obtém e define um valor booliano que indica se os resultados da pesquisa incluem atualizações que são substituídas por outras atualizações nos resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="15762-112">Gets and sets a Boolean value that indicates whether the search results include updates that are superseded by other updates in the search results.</span></span>                                                                                          |
| [<span data-ttu-id="15762-113">**Online**</span><span class="sxs-lookup"><span data-stu-id="15762-113">**Online**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | <span data-ttu-id="15762-114">Obtém e define um valor booliano que indica se o [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) fica online para Pesquisar atualizações.</span><span class="sxs-lookup"><span data-stu-id="15762-114">Gets and sets a Boolean value that indicates whether the [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) goes online to search for updates.</span></span>                                                                                                        |
| [<span data-ttu-id="15762-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="15762-115">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | <span data-ttu-id="15762-116">Obtém e define um site a ser pesquisado quando o site a ser pesquisado não é um Windows Update site.</span><span class="sxs-lookup"><span data-stu-id="15762-116">Gets and sets a site to search when the site to search is not a Windows Update site.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="15762-117">**ServerSelection**</span><span class="sxs-lookup"><span data-stu-id="15762-117">**ServerSelection**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | <span data-ttu-id="15762-118">Obtém e define um valor de [**Serverselection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) que indica o servidor para procurar atualizações.</span><span class="sxs-lookup"><span data-stu-id="15762-118">Gets and sets a [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) value that indicates the server to search for updates.</span></span>                                                                                                                            |




 

 

 



