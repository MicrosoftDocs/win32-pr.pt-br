---
title: Método MyItem. getstatistics
description: Recupera os valores médio, máximo e mínimo para o contador.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Método getstatistics SysMon
- Método getstatistics SysMon, classe de coitem
- Classe monoitem SysMon, método getstatistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918577"
---
# <a name="counteritemgetstatistics-method"></a><span data-ttu-id="f51c1-106">Método MyItem. getstatistics</span><span class="sxs-lookup"><span data-stu-id="f51c1-106">CounterItem.GetStatistics method</span></span>

<span data-ttu-id="f51c1-107">Recupera os valores médio, máximo e mínimo para o contador.</span><span class="sxs-lookup"><span data-stu-id="f51c1-107">Retrieves the average, maximum, and minimum values for the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f51c1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f51c1-108">Syntax</span></span>


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="f51c1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f51c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f51c1-110">*máximo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f51c1-110">*max* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f51c1-111">Valor máximo do contador.</span><span class="sxs-lookup"><span data-stu-id="f51c1-111">Maximum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="f51c1-112">*mín* \[ . fora\]</span><span class="sxs-lookup"><span data-stu-id="f51c1-112">*min* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f51c1-113">Valor mínimo do contador.</span><span class="sxs-lookup"><span data-stu-id="f51c1-113">Minimum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="f51c1-114">*média* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f51c1-114">*average* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f51c1-115">Valor médio do contador.</span><span class="sxs-lookup"><span data-stu-id="f51c1-115">Average value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="f51c1-116">*status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f51c1-116">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f51c1-117">Indica se os valores são válidos.</span><span class="sxs-lookup"><span data-stu-id="f51c1-117">Indicates if the values are valid.</span></span>



| <span data-ttu-id="f51c1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f51c1-118">Value</span></span>                                                                                              | <span data-ttu-id="f51c1-119">Significado</span><span class="sxs-lookup"><span data-stu-id="f51c1-119">Meaning</span></span>                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="f51c1-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f51c1-120"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f51c1-121">Os valores são válidos.</span><span class="sxs-lookup"><span data-stu-id="f51c1-121">The values are valid.</span></span><br/>     |
| <dl> <span data-ttu-id="f51c1-122"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="f51c1-122"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="f51c1-123">Os valores não são válidos.</span><span class="sxs-lookup"><span data-stu-id="f51c1-123">The values are not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f51c1-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f51c1-124">Return value</span></span>

<span data-ttu-id="f51c1-125">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f51c1-125">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f51c1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f51c1-126">Remarks</span></span>

<span data-ttu-id="f51c1-127">Somente os valores de contador visíveis na janela do Graph são usados para calcular os valores estatísticos.</span><span class="sxs-lookup"><span data-stu-id="f51c1-127">Only those counter values that are visible in the graph window are used to calculate the statistical values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f51c1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f51c1-128">Requirements</span></span>



| <span data-ttu-id="f51c1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51c1-129">Requirement</span></span> | <span data-ttu-id="f51c1-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f51c1-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f51c1-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f51c1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f51c1-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f51c1-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f51c1-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f51c1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f51c1-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f51c1-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f51c1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f51c1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f51c1-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f51c1-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f51c1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f51c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51c1-138">**Item**</span><span class="sxs-lookup"><span data-stu-id="f51c1-138">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="f51c1-139">**MYITEM. GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="f51c1-139">**CounterItem.GetDataAt**</span></span>](counteritem-getdataat.md)
</dt> <dt>

[<span data-ttu-id="f51c1-140">**MYITEM. GetValue**</span><span class="sxs-lookup"><span data-stu-id="f51c1-140">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





