---
title: Métodos de propriedade IADsLargeInteger (IADs. h)
description: Os métodos de propriedade da interface IADsLargeInteger obtêm e definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsLargeInteger
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097e9ae7387658f983c691e56e4f90ba40dea407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753618"
---
# <a name="iadslargeinteger-property-methods"></a><span data-ttu-id="64220-105">Métodos de propriedade IADsLargeInteger</span><span class="sxs-lookup"><span data-stu-id="64220-105">IADsLargeInteger Property Methods</span></span>

<span data-ttu-id="64220-106">Os métodos de propriedade da interface [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) obtêm e definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="64220-106">The property methods of the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface get and set the properties described in the following table.</span></span> <span data-ttu-id="64220-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="64220-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="64220-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64220-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="64220-109">**HighPart**</span><span class="sxs-lookup"><span data-stu-id="64220-109">**HighPart**</span></span>
<span data-ttu-id="64220-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="64220-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="64220-111">A parte superior do inteiro.</span><span class="sxs-lookup"><span data-stu-id="64220-111">The high part of the integer.</span></span>

<dt>

<span data-ttu-id="64220-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="64220-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="64220-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="64220-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="64220-114">**LowPart**</span><span class="sxs-lookup"><span data-stu-id="64220-114">**LowPart**</span></span>
<span data-ttu-id="64220-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="64220-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="64220-116">A parte inferior do inteiro.</span><span class="sxs-lookup"><span data-stu-id="64220-116">The low part of the integer.</span></span>

<dt>

<span data-ttu-id="64220-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="64220-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="64220-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="64220-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="64220-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="64220-119">Remarks</span></span>

<span data-ttu-id="64220-120">Se largeInt for do tipo **LargeInteger** , seu valor será especificado por aqueles de **HighPart** e **LowPart** de acordo com a fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="64220-120">If largeInt is of the **LargeInteger** type, its value is specified by those of **HighPart** and **LowPart** according to the following formula.</span></span>


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a><span data-ttu-id="64220-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64220-121">Examples</span></span>

<span data-ttu-id="64220-122">O exemplo de código a seguir Visual Basic define um inteiro grande como 43937327281.</span><span class="sxs-lookup"><span data-stu-id="64220-122">The following Visual Basic code example sets a large integer to 43937327281.</span></span>


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a><span data-ttu-id="64220-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64220-123">Requirements</span></span>



| <span data-ttu-id="64220-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="64220-124">Requirement</span></span> | <span data-ttu-id="64220-125">Valor</span><span class="sxs-lookup"><span data-stu-id="64220-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64220-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64220-126">Minimum supported client</span></span><br/> | <span data-ttu-id="64220-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64220-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64220-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64220-128">Minimum supported server</span></span><br/> | <span data-ttu-id="64220-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64220-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64220-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64220-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="64220-131"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="64220-131"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="64220-132">DLL</span><span class="sxs-lookup"><span data-stu-id="64220-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64220-133"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64220-133"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="64220-134">IID</span><span class="sxs-lookup"><span data-stu-id="64220-134">IID</span></span><br/>                      | <span data-ttu-id="64220-135">IID \_ IADsLargeInteger é definido como 9068270B-0939-11D1-8BE1-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="64220-135">IID\_IADsLargeInteger is defined as 9068270B-0939-11D1-8BE1-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="64220-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="64220-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64220-137">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="64220-137">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





