---
title: Métodos de propriedade IADsTimestamp (IADs. h)
description: O método Property da interface IADsTimestamp define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsTimestamp
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455023"
---
# <a name="iadstimestamp-property-methods"></a><span data-ttu-id="6d9d3-105">Métodos de propriedade IADsTimestamp</span><span class="sxs-lookup"><span data-stu-id="6d9d3-105">IADsTimestamp Property Methods</span></span>

<span data-ttu-id="6d9d3-106">O método Property da interface [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d9d3-106">The property method of the [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) interface sets the property described in the following table.</span></span> <span data-ttu-id="6d9d3-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6d9d3-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6d9d3-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6d9d3-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6d9d3-109">**EventID**</span><span class="sxs-lookup"><span data-stu-id="6d9d3-109">**EventID**</span></span>
<span data-ttu-id="6d9d3-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6d9d3-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6d9d3-111">Um identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="6d9d3-111">An event identifier.</span></span>

<dt>

<span data-ttu-id="6d9d3-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6d9d3-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6d9d3-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="6d9d3-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d9d3-114">**WholeSeconds**</span><span class="sxs-lookup"><span data-stu-id="6d9d3-114">**WholeSeconds**</span></span>
<span data-ttu-id="6d9d3-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6d9d3-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="6d9d3-116">Número de segundos com valor zero de 12:00 A.M., 1970 de janeiro de UTC.</span><span class="sxs-lookup"><span data-stu-id="6d9d3-116">Number of seconds with zero value being 12:00 AM, January 1970, UTC.</span></span>

<dt>

<span data-ttu-id="6d9d3-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="6d9d3-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6d9d3-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="6d9d3-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="6d9d3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d9d3-119">Requirements</span></span>



| <span data-ttu-id="6d9d3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d9d3-120">Requirement</span></span> | <span data-ttu-id="6d9d3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6d9d3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9d3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d9d3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9d3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d9d3-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d9d3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d9d3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9d3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d9d3-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d9d3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d9d3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d9d3-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d9d3-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6d9d3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6d9d3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d9d3-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d9d3-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6d9d3-130">IID</span><span class="sxs-lookup"><span data-stu-id="6d9d3-130">IID</span></span><br/>                      | <span data-ttu-id="6d9d3-131">IID \_ IADsTimestamp é definido como B2F5A901-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="6d9d3-131">IID\_IADsTimestamp is defined as B2F5A901-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6d9d3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d9d3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9d3-133">**IADsTimestamp**</span><span class="sxs-lookup"><span data-stu-id="6d9d3-133">**IADsTimestamp**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[<span data-ttu-id="6d9d3-134">**\_carimbo de data/hora ADS**</span><span class="sxs-lookup"><span data-stu-id="6d9d3-134">**ADS\_TIMESTAMP**</span></span>](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





