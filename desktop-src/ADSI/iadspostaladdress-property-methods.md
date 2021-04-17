---
title: Métodos de propriedade IADsPostalAddress (IADs. h)
description: O método Property da interface IADsPostalAddress define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPostalAddress
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d8eeaac8fa258a2df1452b8aa261ee59b3cc85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756070"
---
# <a name="iadspostaladdress-property-methods"></a><span data-ttu-id="b384c-105">Métodos de propriedade IADsPostalAddress</span><span class="sxs-lookup"><span data-stu-id="b384c-105">IADsPostalAddress Property Methods</span></span>

<span data-ttu-id="b384c-106">O método Property da interface [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b384c-106">The property method of the [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) interface sets the property described in the following table.</span></span> <span data-ttu-id="b384c-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b384c-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="b384c-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b384c-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="b384c-109">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="b384c-109">**PostalAddress**</span></span>
<span data-ttu-id="b384c-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="b384c-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="b384c-111">Uma matriz de seis cadeias de caracteres que contêm o endereço postal do usuário.</span><span class="sxs-lookup"><span data-stu-id="b384c-111">An array of six strings holding the postal address of the user.</span></span>

<dt>

<span data-ttu-id="b384c-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b384c-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b384c-113">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b384c-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="b384c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b384c-114">Requirements</span></span>



| <span data-ttu-id="b384c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b384c-115">Requirement</span></span> | <span data-ttu-id="b384c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b384c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b384c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b384c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b384c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b384c-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b384c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b384c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b384c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b384c-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b384c-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b384c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b384c-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="b384c-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="b384c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b384c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b384c-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b384c-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="b384c-125">IID</span><span class="sxs-lookup"><span data-stu-id="b384c-125">IID</span></span><br/>                      | <span data-ttu-id="b384c-126">IID \_ IADsPostalAddress é definido como 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="b384c-126">IID\_IADsPostalAddress is defined as 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="b384c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b384c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b384c-128">**IADsPostalAddress**</span><span class="sxs-lookup"><span data-stu-id="b384c-128">**IADsPostalAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[<span data-ttu-id="b384c-129">**\_POSTALADDRESS ADS**</span><span class="sxs-lookup"><span data-stu-id="b384c-129">**ADS\_POSTALADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 





