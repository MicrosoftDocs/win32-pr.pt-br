---
title: Interface IWMDRMProvider
description: A interface IWMDRMProvider fornece um método que cria os outros objetos das APIs estendidas do Microsoft Windows Media DRM Client. você pode obter um ponteiro para uma instância dessa interface chamando a função WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Formato de mídia do Windows da interface IWMDRMProvider
- Formato de mídia do Windows da interface IWMDRMProvider, descrito
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641578"
---
# <a name="iwmdrmprovider-interface"></a><span data-ttu-id="ee92b-105">Interface IWMDRMProvider</span><span class="sxs-lookup"><span data-stu-id="ee92b-105">IWMDRMProvider interface</span></span>

<span data-ttu-id="ee92b-106">A interface **IWMDRMProvider** fornece um método que cria os outros objetos das APIs estendidas do Microsoft Windows Media DRM Client.</span><span class="sxs-lookup"><span data-stu-id="ee92b-106">The **IWMDRMProvider** interface provides a method that creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="ee92b-107">Você pode obter um ponteiro para uma instância dessa interface chamando a função [**WMDRMCreateProvider**](wmdrmcreateprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="ee92b-107">You can obtain a pointer to an instance of this interface by calling the [**WMDRMCreateProvider**](wmdrmcreateprovider.md) function.</span></span> <span data-ttu-id="ee92b-108">Para obter um ponteiro para uma instância dessa interface que pode criar objetos seguros, você deve chamar a função [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="ee92b-108">To obtain a pointer to an instance of this interface that can create secure objects, you must call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="ee92b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ee92b-109">Members</span></span>

<span data-ttu-id="ee92b-110">A interface **IWMDRMProvider** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ee92b-110">The **IWMDRMProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ee92b-111">**IWMDRMProvider** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ee92b-111">**IWMDRMProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="ee92b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ee92b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ee92b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ee92b-113">Methods</span></span>

<span data-ttu-id="ee92b-114">A interface **IWMDRMProvider** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ee92b-114">The **IWMDRMProvider** interface has these methods.</span></span>



| <span data-ttu-id="ee92b-115">Método</span><span class="sxs-lookup"><span data-stu-id="ee92b-115">Method</span></span>                                              | <span data-ttu-id="ee92b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee92b-116">Description</span></span>                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee92b-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="ee92b-117">**CreateObject**</span></span>](iwmdrmprovider-createobject.md) | <span data-ttu-id="ee92b-118">Recupera um ponteiro para uma interface especificada, criando o objeto de implementação, se necessário.</span><span class="sxs-lookup"><span data-stu-id="ee92b-118">Retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ee92b-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ee92b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee92b-120">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="ee92b-120">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

