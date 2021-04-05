---
title: Método Counters. Remove
description: Remove uma instância de monoitem da coleção.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Remover o método SysMon
- Método de remoção SysMon, classe de contadores
- Classe Counters SysMon, método remove
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918318"
---
# <a name="countersremove-method"></a><span data-ttu-id="c6f48-106">Método Counters. Remove</span><span class="sxs-lookup"><span data-stu-id="c6f48-106">Counters.Remove method</span></span>

<span data-ttu-id="c6f48-107">Remove uma instância de [**monoitem**](counteritem.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="c6f48-107">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f48-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6f48-108">Syntax</span></span>


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="c6f48-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6f48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6f48-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c6f48-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f48-111">Índice do objeto de [**coitem**](counteritem.md) a ser removido da coleção.</span><span class="sxs-lookup"><span data-stu-id="c6f48-111">Index of the [**CounterItem**](counteritem.md) object to remove from the collection.</span></span> <span data-ttu-id="c6f48-112">O índice é baseado em um.</span><span class="sxs-lookup"><span data-stu-id="c6f48-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6f48-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6f48-113">Return value</span></span>

<span data-ttu-id="c6f48-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c6f48-114">This method does not return a value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="c6f48-115">Exceções</span><span class="sxs-lookup"><span data-stu-id="c6f48-115">Exceptions</span></span>



| <span data-ttu-id="c6f48-116">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="c6f48-116">Exception type</span></span>                                  | <span data-ttu-id="c6f48-117">Condição</span><span class="sxs-lookup"><span data-stu-id="c6f48-117">Condition</span></span>                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c6f48-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="c6f48-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="c6f48-119">O índice especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="c6f48-119">The specified index is not valid.</span></span> <span data-ttu-id="c6f48-120">O valor Err. Number é???.</span><span class="sxs-lookup"><span data-stu-id="c6f48-120">The Err.Number value is ???.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c6f48-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6f48-121">Remarks</span></span>

<span data-ttu-id="c6f48-122">Para remover todos os contadores da coleção, você pode chamar [**SystemMonitor. Reset**](systemmonitor-reset.md).</span><span class="sxs-lookup"><span data-stu-id="c6f48-122">To remove all counters from the collection, you can call [**SystemMonitor.Reset**](systemmonitor-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6f48-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6f48-123">Requirements</span></span>



| <span data-ttu-id="c6f48-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f48-124">Requirement</span></span> | <span data-ttu-id="c6f48-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c6f48-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f48-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6f48-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f48-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c6f48-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c6f48-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6f48-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f48-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c6f48-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6f48-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c6f48-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6f48-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c6f48-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6f48-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6f48-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f48-133">**Contadores**</span><span class="sxs-lookup"><span data-stu-id="c6f48-133">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="c6f48-134">**SystemMonitor. Reset**</span><span class="sxs-lookup"><span data-stu-id="c6f48-134">**SystemMonitor.Reset**</span></span>](systemmonitor-reset.md)
</dt> </dl>

 

 





