---
title: Método MyItem. GetValue
description: Recupera o último valor do contador.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- Método @ value SysMon
- Método GetValue SysMon, classe monoitem
- Classe monoitem SysMon, método GetValue
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749430"
---
# <a name="counteritemgetvalue-method"></a><span data-ttu-id="9d32a-106">Método MyItem. GetValue</span><span class="sxs-lookup"><span data-stu-id="9d32a-106">CounterItem.GetValue method</span></span>

<span data-ttu-id="9d32a-107">Recupera o último valor do contador.</span><span class="sxs-lookup"><span data-stu-id="9d32a-107">Retrieves the last value of the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d32a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d32a-108">Syntax</span></span>


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="9d32a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d32a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d32a-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9d32a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d32a-111">Último valor de amostra do contador.</span><span class="sxs-lookup"><span data-stu-id="9d32a-111">Last sampled value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="9d32a-112">*status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9d32a-112">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d32a-113">Indica se o valor é válido.</span><span class="sxs-lookup"><span data-stu-id="9d32a-113">Indicates if the value is valid.</span></span>



| <span data-ttu-id="9d32a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9d32a-114">Value</span></span>                                                                                              | <span data-ttu-id="9d32a-115">Significado</span><span class="sxs-lookup"><span data-stu-id="9d32a-115">Meaning</span></span>                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="9d32a-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9d32a-116"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="9d32a-117">O valor é válido.</span><span class="sxs-lookup"><span data-stu-id="9d32a-117">The value is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="9d32a-118"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="9d32a-118"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="9d32a-119">O valor não é válido.</span><span class="sxs-lookup"><span data-stu-id="9d32a-119">The value is not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d32a-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d32a-120">Return value</span></span>

<span data-ttu-id="9d32a-121">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9d32a-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d32a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d32a-122">Remarks</span></span>

<span data-ttu-id="9d32a-123">Se a origem dos dados do contador for de um arquivo de log, o valor será o último valor do contador no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="9d32a-123">If the source of the counter data is from a log file, the value is the last counter value in the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d32a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d32a-124">Requirements</span></span>



| <span data-ttu-id="9d32a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d32a-125">Requirement</span></span> | <span data-ttu-id="9d32a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9d32a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d32a-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d32a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9d32a-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d32a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9d32a-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d32a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9d32a-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d32a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d32a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9d32a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d32a-132"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9d32a-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d32a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d32a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d32a-134">**Item**</span><span class="sxs-lookup"><span data-stu-id="9d32a-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="9d32a-135">**MYITEM. getstatistics**</span><span class="sxs-lookup"><span data-stu-id="9d32a-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="9d32a-136">**MYITEM. Value**</span><span class="sxs-lookup"><span data-stu-id="9d32a-136">**CounterItem.Value**</span></span>](counteritem-value.md)
</dt> </dl>

 

 





