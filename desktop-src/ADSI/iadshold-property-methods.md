---
title: Métodos de propriedade IADsHold (IADs. h)
description: O método Property da interface IADsHold define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsHold
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae2499efb461e6c13397fdaef75e515f0a1a21a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086041"
---
# <a name="iadshold-property-methods"></a><span data-ttu-id="8fc64-105">Métodos de propriedade IADsHold</span><span class="sxs-lookup"><span data-stu-id="8fc64-105">IADsHold Property Methods</span></span>

<span data-ttu-id="8fc64-106">O método Property da interface [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8fc64-106">The property method of the [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) interface sets the property described in the following table.</span></span> <span data-ttu-id="8fc64-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8fc64-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="8fc64-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8fc64-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="8fc64-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8fc64-109">**Amount**</span></span>
<span data-ttu-id="8fc64-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8fc64-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="8fc64-111">A quantidade de encargos arrecadados em relação ao usuário para o período em espera enquanto o servidor verifica o saldo da conta do usuário.</span><span class="sxs-lookup"><span data-stu-id="8fc64-111">The amount of charges levied against the user for the period on hold while the server checks the account balance of the user.</span></span>

<dt>

<span data-ttu-id="8fc64-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8fc64-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8fc64-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="8fc64-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="8fc64-114">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="8fc64-114">**ObjectName**</span></span>
<span data-ttu-id="8fc64-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="8fc64-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="8fc64-116">O nome do objeto que representa um usuário em espera.</span><span class="sxs-lookup"><span data-stu-id="8fc64-116">The name of the object representing a user on hold.</span></span>

<dt>

<span data-ttu-id="8fc64-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8fc64-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8fc64-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8fc64-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="8fc64-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fc64-119">Requirements</span></span>



| <span data-ttu-id="8fc64-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc64-120">Requirement</span></span> | <span data-ttu-id="8fc64-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc64-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc64-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fc64-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc64-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fc64-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fc64-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fc64-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc64-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fc64-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fc64-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8fc64-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc64-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc64-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="8fc64-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc64-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fc64-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc64-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="8fc64-130">IID</span><span class="sxs-lookup"><span data-stu-id="8fc64-130">IID</span></span><br/>                      | <span data-ttu-id="8fc64-131">IID \_ IADsHold é definido como B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="8fc64-131">IID\_IADsHold is defined as B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8fc64-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fc64-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc64-133">**IADsHold**</span><span class="sxs-lookup"><span data-stu-id="8fc64-133">**IADsHold**</span></span>](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





