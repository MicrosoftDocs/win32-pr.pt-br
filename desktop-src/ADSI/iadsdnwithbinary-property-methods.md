---
title: Métodos de propriedade IADsDNWithBinary (IADs. h)
description: O método Property da interface IADsDNWithBinary define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsDNWithBinary
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086045"
---
# <a name="iadsdnwithbinary-property-methods"></a><span data-ttu-id="31f4c-105">Métodos de propriedade IADsDNWithBinary</span><span class="sxs-lookup"><span data-stu-id="31f4c-105">IADsDNWithBinary Property Methods</span></span>

<span data-ttu-id="31f4c-106">O método Property da interface [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="31f4c-106">The property method of the [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) interface sets the property described in the following table.</span></span> <span data-ttu-id="31f4c-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="31f4c-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="31f4c-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31f4c-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="31f4c-109">**Bináriovalue**</span><span class="sxs-lookup"><span data-stu-id="31f4c-109">**BinaryValue**</span></span>
<span data-ttu-id="31f4c-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="31f4c-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="31f4c-111">O GUID de um objeto associado a um DN.</span><span class="sxs-lookup"><span data-stu-id="31f4c-111">The GUID of an object associated with a DN.</span></span>

<dt>

<span data-ttu-id="31f4c-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="31f4c-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="31f4c-113">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="31f4c-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="31f4c-114">**DNString**</span><span class="sxs-lookup"><span data-stu-id="31f4c-114">**DNString**</span></span>
<span data-ttu-id="31f4c-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="31f4c-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="31f4c-116">A cadeia de caracteres DN associada ao GUID de um objeto.</span><span class="sxs-lookup"><span data-stu-id="31f4c-116">The DN string associated with the GUID of an object.</span></span>

<dt>

<span data-ttu-id="31f4c-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="31f4c-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="31f4c-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="31f4c-118">Scripting data type: **BSTR**</span></span>
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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="31f4c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f4c-119">Requirements</span></span>



| <span data-ttu-id="31f4c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f4c-120">Requirement</span></span> | <span data-ttu-id="31f4c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="31f4c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31f4c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31f4c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="31f4c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31f4c-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31f4c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31f4c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="31f4c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31f4c-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31f4c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31f4c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="31f4c-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="31f4c-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="31f4c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="31f4c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31f4c-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31f4c-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="31f4c-130">IID</span><span class="sxs-lookup"><span data-stu-id="31f4c-130">IID</span></span><br/>                      | <span data-ttu-id="31f4c-131">IID \_ IADsDNWithBinary é definido como 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span><span class="sxs-lookup"><span data-stu-id="31f4c-131">IID\_IADsDNWithBinary is defined as 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="31f4c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="31f4c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f4c-133">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="31f4c-133">**IADsDNWithBinary**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[<span data-ttu-id="31f4c-134">**ADS \_ DN \_ com \_ binário**</span><span class="sxs-lookup"><span data-stu-id="31f4c-134">**ADS\_DN\_WITH\_BINARY**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 





