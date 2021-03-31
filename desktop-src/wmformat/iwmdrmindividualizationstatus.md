---
title: Interface IWMDRMIndividualizationStatus
description: A interface IWMDRMIndividualizationStatus permite a recuperação de informações de status avançadas sobre o progresso da individualização. Essa interface é fornecida com eventos MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Formato de mídia do Windows da interface IWMDRMIndividualizationStatus
- Formato de mídia do Windows da interface IWMDRMIndividualizationStatus, descrito
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917554"
---
# <a name="iwmdrmindividualizationstatus-interface"></a><span data-ttu-id="95b3b-105">Interface IWMDRMIndividualizationStatus</span><span class="sxs-lookup"><span data-stu-id="95b3b-105">IWMDRMIndividualizationStatus interface</span></span>

<span data-ttu-id="95b3b-106">A interface **IWMDRMIndividualizationStatus** permite a recuperação de informações de status avançadas sobre o progresso da individualização.</span><span class="sxs-lookup"><span data-stu-id="95b3b-106">The **IWMDRMIndividualizationStatus** interface enables retrieval of advanced status information about the progress of individualization.</span></span>

<span data-ttu-id="95b3b-107">Essa interface é fornecida com eventos MEWMDRMIndividualizationProgress.</span><span class="sxs-lookup"><span data-stu-id="95b3b-107">This interface is delivered with MEWMDRMIndividualizationProgress events.</span></span> <span data-ttu-id="95b3b-108">Muitos desses eventos são gerados entre uma chamada para [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) e a conclusão do processo de individualização, que é sinalizado pela geração de um evento **MEWMDRMIndividualizationCompleted** .</span><span class="sxs-lookup"><span data-stu-id="95b3b-108">Many such events are generated between a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) and the completion of the individualization process, which is signaled by the generation of an **MEWMDRMIndividualizationCompleted** event.</span></span>

<span data-ttu-id="95b3b-109">Para recuperar um ponteiro para uma instância da interface **IWMDRMIndividualizationStatus** , você deve primeiro chamar o método **IMFMediaEvent:: GetValue** do evento Progress.</span><span class="sxs-lookup"><span data-stu-id="95b3b-109">To retrieve a pointer to an instance of the **IWMDRMIndividualizationStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="95b3b-110">O valor que você recupera do evento é um ponteiro para a interface **IUnknown** do objeto que implementa a interface **IWMDRMIndividualizationStatus** .</span><span class="sxs-lookup"><span data-stu-id="95b3b-110">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMIndividualizationStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="95b3b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="95b3b-111">Members</span></span>

<span data-ttu-id="95b3b-112">A interface **IWMDRMIndividualizationStatus** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="95b3b-112">The **IWMDRMIndividualizationStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="95b3b-113">**IWMDRMIndividualizationStatus** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="95b3b-113">**IWMDRMIndividualizationStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="95b3b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="95b3b-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="95b3b-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="95b3b-115">Methods</span></span>

<span data-ttu-id="95b3b-116">A interface **IWMDRMIndividualizationStatus** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="95b3b-116">The **IWMDRMIndividualizationStatus** interface has these methods.</span></span>



| <span data-ttu-id="95b3b-117">Método</span><span class="sxs-lookup"><span data-stu-id="95b3b-117">Method</span></span>                                                       | <span data-ttu-id="95b3b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="95b3b-118">Description</span></span>                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="95b3b-119">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="95b3b-119">**GetStatus**</span></span>](iwmdrmindividualizationstatus-getstatus.md) | <span data-ttu-id="95b3b-120">Recupera informações detalhadas sobre individualização.</span><span class="sxs-lookup"><span data-stu-id="95b3b-120">Retrieves detailed information about individualization.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="95b3b-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="95b3b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b3b-122">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="95b3b-122">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

