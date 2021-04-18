---
title: Métodos de propriedade IADsTypedName (IADs. h)
description: O método Property da interface IADsTypedName define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsTypedName
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756493"
---
# <a name="iadstypedname-property-methods"></a><span data-ttu-id="40947-105">Métodos de propriedade IADsTypedName</span><span class="sxs-lookup"><span data-stu-id="40947-105">IADsTypedName Property Methods</span></span>

<span data-ttu-id="40947-106">O método Property da interface [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="40947-106">The property method of the [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) interface sets the property described in the following table.</span></span> <span data-ttu-id="40947-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="40947-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="40947-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="40947-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="40947-109">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="40947-109">**Interval**</span></span>
<span data-ttu-id="40947-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40947-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="40947-111">A frequência de referência do objeto.</span><span class="sxs-lookup"><span data-stu-id="40947-111">The frequency of reference of the object.</span></span>

<dt>

<span data-ttu-id="40947-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="40947-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40947-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="40947-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="40947-114">**Level**</span><span class="sxs-lookup"><span data-stu-id="40947-114">**Level**</span></span>
<span data-ttu-id="40947-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40947-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="40947-116">O nível de prioridade associado ao objeto.</span><span class="sxs-lookup"><span data-stu-id="40947-116">The priority level associated with the object.</span></span>

<dt>

<span data-ttu-id="40947-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="40947-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40947-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="40947-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="40947-119">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="40947-119">**ObjectName**</span></span>
<span data-ttu-id="40947-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="40947-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="40947-121">O nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="40947-121">The name of an object.</span></span>

<dt>

<span data-ttu-id="40947-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="40947-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40947-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="40947-123">Scripting data type: **BSTR**</span></span>
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

 

## <a name="requirements"></a><span data-ttu-id="40947-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40947-124">Requirements</span></span>



| <span data-ttu-id="40947-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="40947-125">Requirement</span></span> | <span data-ttu-id="40947-126">Valor</span><span class="sxs-lookup"><span data-stu-id="40947-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40947-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40947-127">Minimum supported client</span></span><br/> | <span data-ttu-id="40947-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40947-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40947-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40947-129">Minimum supported server</span></span><br/> | <span data-ttu-id="40947-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40947-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40947-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40947-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="40947-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="40947-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="40947-133">DLL</span><span class="sxs-lookup"><span data-stu-id="40947-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40947-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40947-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="40947-135">IID</span><span class="sxs-lookup"><span data-stu-id="40947-135">IID</span></span><br/>                      | <span data-ttu-id="40947-136">IID \_ IADsTypedName é definido como B371A349-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="40947-136">IID\_IADsTypedName is defined as B371A349-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="40947-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="40947-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40947-138">**IADsTypedName**</span><span class="sxs-lookup"><span data-stu-id="40947-138">**IADsTypedName**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[<span data-ttu-id="40947-139">**tipos de anúncios \_**</span><span class="sxs-lookup"><span data-stu-id="40947-139">**ADS\_TYPEDNAME**</span></span>](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 





