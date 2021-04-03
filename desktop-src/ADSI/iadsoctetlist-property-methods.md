---
title: Métodos de propriedade IADsOctetList (IADs. h)
description: O método Property da interface IADsOctetList define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsOctetList
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3631adaf00cf599214296e1792ffab8697ba5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918887"
---
# <a name="iadsoctetlist-property-methods"></a><span data-ttu-id="18506-105">Métodos de propriedade IADsOctetList</span><span class="sxs-lookup"><span data-stu-id="18506-105">IADsOctetList Property Methods</span></span>

<span data-ttu-id="18506-106">O método Property da interface [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="18506-106">The property method of the [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) interface sets the property described in the following table.</span></span> <span data-ttu-id="18506-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="18506-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="18506-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="18506-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="18506-109">**Octetlist**</span><span class="sxs-lookup"><span data-stu-id="18506-109">**OctetList**</span></span>
<span data-ttu-id="18506-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="18506-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="18506-111">Uma sequência ordenada de matrizes de bytes.</span><span class="sxs-lookup"><span data-stu-id="18506-111">An ordered sequence of byte arrays.</span></span>

<dt>

<span data-ttu-id="18506-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="18506-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="18506-113">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="18506-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="18506-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18506-114">Requirements</span></span>



| <span data-ttu-id="18506-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="18506-115">Requirement</span></span> | <span data-ttu-id="18506-116">Valor</span><span class="sxs-lookup"><span data-stu-id="18506-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18506-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18506-117">Minimum supported client</span></span><br/> | <span data-ttu-id="18506-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18506-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18506-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18506-119">Minimum supported server</span></span><br/> | <span data-ttu-id="18506-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18506-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18506-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18506-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="18506-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="18506-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="18506-123">DLL</span><span class="sxs-lookup"><span data-stu-id="18506-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18506-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18506-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="18506-125">IID</span><span class="sxs-lookup"><span data-stu-id="18506-125">IID</span></span><br/>                      | <span data-ttu-id="18506-126">IID \_ IADsOctetList é definido como 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="18506-126">IID\_IADsOctetList is defined as 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="18506-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="18506-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18506-128">**IADsOctetList**</span><span class="sxs-lookup"><span data-stu-id="18506-128">**IADsOctetList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[<span data-ttu-id="18506-129">**\_lista de octetos ADS \_**</span><span class="sxs-lookup"><span data-stu-id="18506-129">**ADS\_OCTET\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 





