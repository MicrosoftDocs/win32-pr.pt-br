---
title: Métodos de propriedade IADsCaseIgnoreList (IADs. h)
description: O método Property da interface IADsCaseIgnoreList define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsCaseIgnoreList
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aabf26508c3e38e117ad25721af8bece5d69b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755738"
---
# <a name="iadscaseignorelist-property-methods"></a><span data-ttu-id="9298f-105">Métodos de propriedade IADsCaseIgnoreList</span><span class="sxs-lookup"><span data-stu-id="9298f-105">IADsCaseIgnoreList Property Methods</span></span>

<span data-ttu-id="9298f-106">O método Property da interface [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9298f-106">The property method of the [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) interface sets the property described in the following table.</span></span> <span data-ttu-id="9298f-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="9298f-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9298f-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9298f-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="9298f-109">**CaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="9298f-109">**CaseIgnoreList**</span></span>
<span data-ttu-id="9298f-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="9298f-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="9298f-111">Uma sequência ordenada de cadeias de caracteres sem distinção entre maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="9298f-111">An ordered sequence of case insensitive strings.</span></span>

<dt>

<span data-ttu-id="9298f-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="9298f-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9298f-113">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9298f-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="9298f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9298f-114">Requirements</span></span>



| <span data-ttu-id="9298f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9298f-115">Requirement</span></span> | <span data-ttu-id="9298f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9298f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9298f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9298f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9298f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9298f-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9298f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9298f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9298f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9298f-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9298f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9298f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9298f-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="9298f-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="9298f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9298f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9298f-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9298f-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="9298f-125">IID</span><span class="sxs-lookup"><span data-stu-id="9298f-125">IID</span></span><br/>                      | <span data-ttu-id="9298f-126">IID \_ IADsCaseIgnoreList é definido como 7B66B533-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="9298f-126">IID\_IADsCaseIgnoreList is defined as 7B66B533-4680-11D1-A3B4-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="9298f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9298f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9298f-128">**IADsCaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="9298f-128">**IADsCaseIgnoreList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[<span data-ttu-id="9298f-129">**\_lista de CASEIGNORE de anúncios \_**</span><span class="sxs-lookup"><span data-stu-id="9298f-129">**ADS\_CASEIGNORE\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





