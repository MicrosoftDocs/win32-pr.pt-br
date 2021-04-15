---
title: Métodos de propriedade IADsFaxNumber (IADs. h)
description: O método Property da interface IADsFaxNumber define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsFaxNumber
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753835"
---
# <a name="iadsfaxnumber-property-methods"></a><span data-ttu-id="54077-105">Métodos de propriedade IADsFaxNumber</span><span class="sxs-lookup"><span data-stu-id="54077-105">IADsFaxNumber Property Methods</span></span>

<span data-ttu-id="54077-106">O método Property da interface [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="54077-106">The property method of the [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) interface sets the property described in the following table.</span></span> <span data-ttu-id="54077-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="54077-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="54077-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="54077-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="54077-109">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="54077-109">**Parameters**</span></span>
<span data-ttu-id="54077-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="54077-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="54077-111">Os parâmetros para o computador de fax.</span><span class="sxs-lookup"><span data-stu-id="54077-111">The parameters for the fax machine.</span></span>

<dt>

<span data-ttu-id="54077-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="54077-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54077-113">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="54077-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="54077-114">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="54077-114">**TelephoneNumber**</span></span>
<span data-ttu-id="54077-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="54077-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="54077-116">O número de telefone do computador de fax.</span><span class="sxs-lookup"><span data-stu-id="54077-116">The telephone number of the fax machine.</span></span>

<dt>

<span data-ttu-id="54077-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="54077-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="54077-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="54077-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="54077-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54077-119">Requirements</span></span>



| <span data-ttu-id="54077-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="54077-120">Requirement</span></span> | <span data-ttu-id="54077-121">Valor</span><span class="sxs-lookup"><span data-stu-id="54077-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54077-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54077-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54077-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54077-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54077-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54077-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54077-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54077-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54077-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54077-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54077-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="54077-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="54077-128">DLL</span><span class="sxs-lookup"><span data-stu-id="54077-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54077-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54077-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="54077-130">IID</span><span class="sxs-lookup"><span data-stu-id="54077-130">IID</span></span><br/>                      | <span data-ttu-id="54077-131">IID \_ IADsFaxNumber é definido como A910DEA9-4680-11D1-0A3B-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="54077-131">IID\_IADsFaxNumber is defined as A910DEA9-4680-11D1-0A3B-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="54077-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="54077-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54077-133">**IADsFaxNumber**</span><span class="sxs-lookup"><span data-stu-id="54077-133">**IADsFaxNumber**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[<span data-ttu-id="54077-134">**\_FAXNUMBER ADS**</span><span class="sxs-lookup"><span data-stu-id="54077-134">**ADS\_FAXNUMBER**</span></span>](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 





