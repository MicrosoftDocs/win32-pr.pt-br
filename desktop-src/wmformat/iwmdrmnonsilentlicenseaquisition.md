---
title: Interface IWMDRMNonSilentLicenseAquisition
description: A interface IWMDRMNonSilentLicenseAquisition fornece métodos que permitem a aquisição de licenças, exigindo a intervenção do usuário. Essa interface pode ser obtida com a execução de uma aquisição de licença não silenciosa.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Formato de mídia do Windows da interface IWMDRMNonSilentLicenseAquisition
- Formato de mídia do Windows da interface IWMDRMNonSilentLicenseAquisition, descrito
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641452"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a><span data-ttu-id="ced54-105">Interface IWMDRMNonSilentLicenseAquisition</span><span class="sxs-lookup"><span data-stu-id="ced54-105">IWMDRMNonSilentLicenseAquisition interface</span></span>

<span data-ttu-id="ced54-106">A interface **IWMDRMNonSilentLicenseAquisition** fornece métodos que permitem a aquisição de licenças, exigindo a intervenção do usuário.</span><span class="sxs-lookup"><span data-stu-id="ced54-106">The **IWMDRMNonSilentLicenseAquisition** interface provides methods that enable license acquisition requiring user intervention.</span></span>

<span data-ttu-id="ced54-107">Essa interface pode ser obtida com a execução de uma aquisição de licença não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="ced54-107">This interface can be obtained by performing non-silent license acquisition.</span></span> <span data-ttu-id="ced54-108">Depois de chamar [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , um evento **MEWMDRMLicenseAcquisitionCompleted** será gerado.</span><span class="sxs-lookup"><span data-stu-id="ced54-108">After you call [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) an **MEWMDRMLicenseAcquisitionCompleted** event will be generated.</span></span> <span data-ttu-id="ced54-109">Chame o método **IMFMediaEvent:: GetValue** do evento para obter um ponteiro para uma interface **IUnknown** que pode ser consultada para um ponteiro para uma instância dessa interface.</span><span class="sxs-lookup"><span data-stu-id="ced54-109">Call the **IMFMediaEvent::GetValue** method of the event to get a pointer to an **IUnknown** interface that can be queried for a pointer to an instance of this interface.</span></span>

## <a name="members"></a><span data-ttu-id="ced54-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ced54-110">Members</span></span>

<span data-ttu-id="ced54-111">A interface **IWMDRMNonSilentLicenseAquisition** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ced54-111">The **IWMDRMNonSilentLicenseAquisition** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ced54-112">**IWMDRMNonSilentLicenseAquisition** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ced54-112">**IWMDRMNonSilentLicenseAquisition** also has these types of members:</span></span>

-   [<span data-ttu-id="ced54-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ced54-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ced54-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="ced54-114">Methods</span></span>

<span data-ttu-id="ced54-115">A interface **IWMDRMNonSilentLicenseAquisition** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ced54-115">The **IWMDRMNonSilentLicenseAquisition** interface has these methods.</span></span>



| <span data-ttu-id="ced54-116">Método</span><span class="sxs-lookup"><span data-stu-id="ced54-116">Method</span></span>                                                                | <span data-ttu-id="ced54-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ced54-117">Description</span></span>                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="ced54-118">**Getchallenge**</span><span class="sxs-lookup"><span data-stu-id="ced54-118">**GetChallenge**</span></span>](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | <span data-ttu-id="ced54-119">Recupera o desafio de licença que deve ser postado no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="ced54-119">Retrieves the license challenge that should be posted to the license server.</span></span><br/> |
| [<span data-ttu-id="ced54-120">**GetURL**</span><span class="sxs-lookup"><span data-stu-id="ced54-120">**GetURL**</span></span>](iwmdrmnonsilentlicenseaquisition-geturl.md)             | <span data-ttu-id="ced54-121">Recupera a URL para a qual o desafio de licença deve ser lançado.</span><span class="sxs-lookup"><span data-stu-id="ced54-121">Retrieves the URL to which the license challenge should be posted.</span></span><br/>           |



 

## <a name="see-also"></a><span data-ttu-id="ced54-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ced54-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced54-123">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="ced54-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ced54-124">**Aquisição de licença não silenciosa**</span><span class="sxs-lookup"><span data-stu-id="ced54-124">**Non-Silent License Acquisition**</span></span>](non-silent-license-acquisition.md)
</dt> </dl>

 

