---
description: Define ou recupera o valor de uma propriedade compartilhada.
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: Classe SharedProperty (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089131"
---
# <a name="sharedproperty-class"></a><span data-ttu-id="2eb4a-103">Classe SharedProperty</span><span class="sxs-lookup"><span data-stu-id="2eb4a-103">SharedProperty class</span></span>

<span data-ttu-id="2eb4a-104">Define ou recupera o valor de uma propriedade compartilhada.</span><span class="sxs-lookup"><span data-stu-id="2eb4a-104">Sets or retrieves the value of a shared property.</span></span>

<span data-ttu-id="2eb4a-105">Para obter informações gerais sobre como usar o Gerenciador de Propriedades compartilhado no COM+, consulte [com+ Shared Gerenciador de propriedades](com--shared-property-manager.md).</span><span class="sxs-lookup"><span data-stu-id="2eb4a-105">For general information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="2eb4a-106">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="2eb4a-106">When to implement</span></span>

<span data-ttu-id="2eb4a-107">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="2eb4a-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="2eb4a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb4a-108">Requirement</span></span> | <span data-ttu-id="2eb4a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="2eb4a-109">Value</span></span> |
|------------|--------------------------------------------|
| <span data-ttu-id="2eb4a-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2eb4a-110">Interfaces</span></span> | [<span data-ttu-id="2eb4a-111">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="2eb4a-111">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a><span data-ttu-id="2eb4a-112">Quando usar</span><span class="sxs-lookup"><span data-stu-id="2eb4a-112">When to use</span></span>

<span data-ttu-id="2eb4a-113">Use essa classe para acessar os métodos de [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span><span class="sxs-lookup"><span data-stu-id="2eb4a-113">Use this class to access the methods of [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span></span>

## <a name="remarks"></a><span data-ttu-id="2eb4a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eb4a-114">Remarks</span></span>

<span data-ttu-id="2eb4a-115">Você pode criar um objeto **SharedProperty** usando os métodos [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) ou [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) de [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span><span class="sxs-lookup"><span data-stu-id="2eb4a-115">You can create a **SharedProperty** object by using the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

<span data-ttu-id="2eb4a-116">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="2eb4a-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="2eb4a-117">Um objeto SharedProperty é criado chamando os métodos [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) ou [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) do objeto [**SharedPropertyGroup**](sharedpropertygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="2eb4a-117">A SharedProperty object is created by calling the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of the [**SharedPropertyGroup**](sharedpropertygroup.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb4a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eb4a-118">Requirements</span></span>



| <span data-ttu-id="2eb4a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb4a-119">Requirement</span></span> | <span data-ttu-id="2eb4a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2eb4a-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb4a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eb4a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb4a-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2eb4a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2eb4a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eb4a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb4a-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2eb4a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2eb4a-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2eb4a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb4a-126"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb4a-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb4a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2eb4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb4a-128">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="2eb4a-128">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[<span data-ttu-id="2eb4a-129">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="2eb4a-129">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> <dt>

[<span data-ttu-id="2eb4a-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="2eb4a-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




