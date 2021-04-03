---
description: A Propriedade IsLocal do objeto SWbemProperty é um valor booliano que pode ser usado para determinar se essa propriedade é local. Um valor FALSE indica que essa propriedade foi herdada de outra classe. Esta propriedade é somente para leitura.
ms.assetid: eda1f962-03b5-4322-bb06-c27aedf94be1
ms.tgt_platform: multiple
title: Propriedade SWbemProperty. IsLocal (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.IsLocal
- ISWbemProperty.IsLocal
- ISWbemProperty.get_IsLocal
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 187613a0111c7ad482c55e3d294d77fddb5b0941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828658"
---
# <a name="swbempropertyislocal-property"></a><span data-ttu-id="5814c-105">Propriedade SWbemProperty. IsLocal</span><span class="sxs-lookup"><span data-stu-id="5814c-105">SWbemProperty.IsLocal property</span></span>

<span data-ttu-id="5814c-106">A propriedade **IsLocal** do objeto [**SWbemProperty**](swbemproperty.md) é um valor booliano que pode ser usado para determinar se essa propriedade é local.</span><span class="sxs-lookup"><span data-stu-id="5814c-106">The **IsLocal** property of the [**SWbemProperty**](swbemproperty.md) object is a Boolean value that can be used to determine if this property is local.</span></span> <span data-ttu-id="5814c-107">Um valor **false** indica que essa propriedade foi herdada de outra classe.</span><span class="sxs-lookup"><span data-stu-id="5814c-107">A value of **FALSE** indicates that this property has been inherited from another class.</span></span> <span data-ttu-id="5814c-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5814c-108">This property is read-only.</span></span>

<span data-ttu-id="5814c-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5814c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5814c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5814c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5814c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5814c-111">Syntax</span></span>


```VB
SWbemProperty.IsLocal As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5814c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5814c-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="5814c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5814c-113">Requirements</span></span>



| <span data-ttu-id="5814c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5814c-114">Requirement</span></span> | <span data-ttu-id="5814c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5814c-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5814c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5814c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5814c-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5814c-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5814c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5814c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5814c-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5814c-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5814c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5814c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5814c-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5814c-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5814c-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5814c-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5814c-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5814c-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5814c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5814c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5814c-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5814c-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5814c-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="5814c-126">CLSID</span></span><br/>                    | <span data-ttu-id="5814c-127">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="5814c-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="5814c-128">IID</span><span class="sxs-lookup"><span data-stu-id="5814c-128">IID</span></span><br/>                      | <span data-ttu-id="5814c-129">ISWbemProperty de IID \_</span><span class="sxs-lookup"><span data-stu-id="5814c-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




