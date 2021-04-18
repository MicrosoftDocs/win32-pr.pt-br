---
description: A propriedade Parameters do objeto SWbemMethod é um objeto SWbemObject cujas propriedades definem os parâmetros de entrada para esse método.
ms.assetid: fba1bb97-29f9-41d3-8ecc-f283989118c1
ms.tgt_platform: multiple
title: Propriedade SWbemMethod. Parameters (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.InParameters
- ISWbemMethod.InParameters
- ISWbemMethod.get_InParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8df897f876673f6b4afe875e718401ae4c217e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796119"
---
# <a name="swbemmethodinparameters-property"></a><span data-ttu-id="52654-103">Propriedade SWbemMethod. Parameters</span><span class="sxs-lookup"><span data-stu-id="52654-103">SWbemMethod.InParameters property</span></span>

<span data-ttu-id="52654-104">A propriedade **Parameters** do objeto [**SWbemMethod**](swbemmethod.md) é um objeto [**SWbemObject**](swbemobject.md) cujas propriedades definem os parâmetros de entrada para esse método.</span><span class="sxs-lookup"><span data-stu-id="52654-104">The **InParameters** property of the [**SWbemMethod**](swbemmethod.md) object is an [**SWbemObject**](swbemobject.md) object whose properties define the input parameters for this method.</span></span> <span data-ttu-id="52654-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="52654-105">This property is read-only.</span></span> <span data-ttu-id="52654-106">Observe que as alterações feitas a esse objeto não são refletidas na definição do método subjacente.</span><span class="sxs-lookup"><span data-stu-id="52654-106">Note that any changes that are made to this object are not reflected in the underlying method definition.</span></span>

<span data-ttu-id="52654-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="52654-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="52654-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="52654-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52654-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52654-109">Syntax</span></span>


```VB
SWbemMethod.InParameters As Object
```



## <a name="property-value"></a><span data-ttu-id="52654-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52654-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="52654-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="52654-111">Remarks</span></span>

<span data-ttu-id="52654-112">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="52654-112">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52654-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52654-113">Requirements</span></span>



| <span data-ttu-id="52654-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52654-114">Requirement</span></span> | <span data-ttu-id="52654-115">Valor</span><span class="sxs-lookup"><span data-stu-id="52654-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52654-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52654-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52654-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52654-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52654-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52654-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52654-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52654-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52654-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52654-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52654-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="52654-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="52654-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="52654-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="52654-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="52654-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="52654-124">DLL</span><span class="sxs-lookup"><span data-stu-id="52654-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52654-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52654-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="52654-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="52654-126">CLSID</span></span><br/>                    | <span data-ttu-id="52654-127">\_SWBEMMETHOD CLSID</span><span class="sxs-lookup"><span data-stu-id="52654-127">CLSID\_SWbemMethod</span></span><br/>                                                           |
| <span data-ttu-id="52654-128">IID</span><span class="sxs-lookup"><span data-stu-id="52654-128">IID</span></span><br/>                      | <span data-ttu-id="52654-129">ISWbemMethod de IID \_</span><span class="sxs-lookup"><span data-stu-id="52654-129">IID\_ISWbemMethod</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="52654-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="52654-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52654-131">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="52654-131">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> <dt>

[<span data-ttu-id="52654-132">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="52654-132">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="52654-133">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="52654-133">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="52654-134">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="52654-134">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="52654-135">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="52654-135">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




