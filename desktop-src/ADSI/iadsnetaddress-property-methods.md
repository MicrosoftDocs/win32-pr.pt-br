---
title: Métodos de propriedade IADsNetAddress (IADs. h)
description: O método Property da interface IADsNetAddress define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsNetAddress
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073033c703db8eaa55b05058d6d2bbc3d3167f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644947"
---
# <a name="iadsnetaddress-property-methods"></a><span data-ttu-id="81fcf-105">Métodos de propriedade IADsNetAddress</span><span class="sxs-lookup"><span data-stu-id="81fcf-105">IADsNetAddress Property Methods</span></span>

<span data-ttu-id="81fcf-106">O método Property da interface [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="81fcf-106">The property method of the [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) interface sets the property described in the following table.</span></span> <span data-ttu-id="81fcf-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="81fcf-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="81fcf-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="81fcf-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="81fcf-109">**Endereço**</span><span class="sxs-lookup"><span data-stu-id="81fcf-109">**Address**</span></span>
<span data-ttu-id="81fcf-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="81fcf-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="81fcf-111">Um endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="81fcf-111">A network address.</span></span>

<dt>

<span data-ttu-id="81fcf-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81fcf-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="81fcf-113">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="81fcf-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="81fcf-114">**AddressType**</span><span class="sxs-lookup"><span data-stu-id="81fcf-114">**AddressType**</span></span>
<span data-ttu-id="81fcf-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="81fcf-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="81fcf-116">Um tipo de protocolos de comunicação.</span><span class="sxs-lookup"><span data-stu-id="81fcf-116">A type of communication protocols.</span></span>

<dt>

<span data-ttu-id="81fcf-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="81fcf-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="81fcf-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="81fcf-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="81fcf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81fcf-119">Requirements</span></span>



| <span data-ttu-id="81fcf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="81fcf-120">Requirement</span></span> | <span data-ttu-id="81fcf-121">Valor</span><span class="sxs-lookup"><span data-stu-id="81fcf-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81fcf-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81fcf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="81fcf-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81fcf-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81fcf-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81fcf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="81fcf-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81fcf-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81fcf-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81fcf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="81fcf-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="81fcf-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="81fcf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="81fcf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81fcf-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81fcf-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="81fcf-130">IID</span><span class="sxs-lookup"><span data-stu-id="81fcf-130">IID</span></span><br/>                      | <span data-ttu-id="81fcf-131">IID \_ IADsNetAddress é definido como B21A50A9-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="81fcf-131">IID\_IADsNetAddress is defined as B21A50A9-4080-11D1-A3AC-00C04FB950DC</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="81fcf-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="81fcf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81fcf-133">**IADsNetAddress**</span><span class="sxs-lookup"><span data-stu-id="81fcf-133">**IADsNetAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[<span data-ttu-id="81fcf-134">**Endereço netads \_**</span><span class="sxs-lookup"><span data-stu-id="81fcf-134">**ADS\_NETADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 





