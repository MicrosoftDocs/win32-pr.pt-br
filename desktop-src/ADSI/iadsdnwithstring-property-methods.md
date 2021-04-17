---
title: Métodos de propriedade IADsDNWithString (IADs. h)
description: O método Property da interface IADsDNWithString define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsDNWithString
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa63a933a6a41eec9e6e55906a940cee650c87b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754886"
---
# <a name="iadsdnwithstring-property-methods"></a><span data-ttu-id="978dd-105">Métodos de propriedade IADsDNWithString</span><span class="sxs-lookup"><span data-stu-id="978dd-105">IADsDNWithString Property Methods</span></span>

<span data-ttu-id="978dd-106">O método Property da interface [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="978dd-106">The property method of the [**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) interface sets the property described in the following table.</span></span> <span data-ttu-id="978dd-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="978dd-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="978dd-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="978dd-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="978dd-109">**DNString**</span><span class="sxs-lookup"><span data-stu-id="978dd-109">**DNString**</span></span>
<span data-ttu-id="978dd-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="978dd-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="978dd-111">A cadeia de caracteres DN associada a um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="978dd-111">The DN string associated with a string value.</span></span>

<dt>

<span data-ttu-id="978dd-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="978dd-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="978dd-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="978dd-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="978dd-114">**StringValue**</span><span class="sxs-lookup"><span data-stu-id="978dd-114">**StringValue**</span></span>
<span data-ttu-id="978dd-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="978dd-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="978dd-116">O valor da cadeia de caracteres associada a um DN de um objeto.</span><span class="sxs-lookup"><span data-stu-id="978dd-116">The string value associated with a DN of an object.</span></span>

<dt>

<span data-ttu-id="978dd-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="978dd-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="978dd-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="978dd-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="978dd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="978dd-119">Requirements</span></span>



| <span data-ttu-id="978dd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="978dd-120">Requirement</span></span> | <span data-ttu-id="978dd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="978dd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="978dd-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="978dd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="978dd-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="978dd-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="978dd-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="978dd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="978dd-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="978dd-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="978dd-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="978dd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="978dd-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="978dd-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="978dd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="978dd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="978dd-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="978dd-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="978dd-130">IID</span><span class="sxs-lookup"><span data-stu-id="978dd-130">IID</span></span><br/>                      | <span data-ttu-id="978dd-131">IID \_ IADsDNWithString é definido como 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="978dd-131">IID\_IADsDNWithString is defined as 370DF02E-F934-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="978dd-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="978dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978dd-133">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="978dd-133">**IADsDNWithString**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[<span data-ttu-id="978dd-134">**\_DN ADS \_ com \_ cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="978dd-134">**ADS\_DN\_WITH\_STRING**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 





