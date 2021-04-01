---
description: Cria e acessa as propriedades compartilhadas em um grupo de propriedades compartilhado.
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: Classe SharedPropertyGroup (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646317"
---
# <a name="sharedpropertygroup-class"></a><span data-ttu-id="1d2e3-103">Classe SharedPropertyGroup</span><span class="sxs-lookup"><span data-stu-id="1d2e3-103">SharedPropertyGroup class</span></span>

<span data-ttu-id="1d2e3-104">Cria e acessa as propriedades compartilhadas em um grupo de propriedades compartilhado.</span><span class="sxs-lookup"><span data-stu-id="1d2e3-104">Creates and accesses the shared properties in a shared property group.</span></span>

<span data-ttu-id="1d2e3-105">Para obter mais informações sobre como usar o Gerenciador de Propriedades compartilhado no COM+, consulte [com+ Shared Gerenciador de propriedades](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="1d2e3-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="1d2e3-106">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="1d2e3-106">When to implement</span></span>

<span data-ttu-id="1d2e3-107">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="1d2e3-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="1d2e3-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d2e3-108">Requirement</span></span> | <span data-ttu-id="1d2e3-109">Valor</span><span class="sxs-lookup"><span data-stu-id="1d2e3-109">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="1d2e3-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="1d2e3-110">Interfaces</span></span> | [<span data-ttu-id="1d2e3-111">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="1d2e3-111">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a><span data-ttu-id="1d2e3-112">Quando usar</span><span class="sxs-lookup"><span data-stu-id="1d2e3-112">When to use</span></span>

<span data-ttu-id="1d2e3-113">Use essa classe para acessar os métodos de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="1d2e3-113">Use this class to access the methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d2e3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d2e3-114">Remarks</span></span>

<span data-ttu-id="1d2e3-115">Você pode criar um objeto **SharedPropertyGroup** usando o método [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) do [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span><span class="sxs-lookup"><span data-stu-id="1d2e3-115">You can create a **SharedPropertyGroup** object using the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

<span data-ttu-id="1d2e3-116">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="1d2e3-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="1d2e3-117">Um objeto SharedPropertyGroup é criado chamando o método [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) do objeto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="1d2e3-117">A SharedPropertyGroup object is created by calling the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2e3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d2e3-118">Requirements</span></span>



| <span data-ttu-id="1d2e3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d2e3-119">Requirement</span></span> | <span data-ttu-id="1d2e3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1d2e3-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2e3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d2e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2e3-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1d2e3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1d2e3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d2e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2e3-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1d2e3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1d2e3-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1d2e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d2e3-126"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d2e3-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d2e3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d2e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2e3-128">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="1d2e3-128">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[<span data-ttu-id="1d2e3-129">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="1d2e3-129">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="1d2e3-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="1d2e3-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




