---
title: Propriedade Counters. Item
description: Recupera a instância de monoitem especificada da coleção.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Propriedade do item SysMon
- Propriedade de item SysMon, classe de contadores
- Classe Counters SysMon, Propriedade Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454849"
---
# <a name="countersitem-property"></a><span data-ttu-id="2b59c-106">Propriedade Counters. Item</span><span class="sxs-lookup"><span data-stu-id="2b59c-106">Counters.Item property</span></span>

<span data-ttu-id="2b59c-107">Recupera a instância de [**monoitem**](counteritem.md) especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="2b59c-107">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span>

<span data-ttu-id="2b59c-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2b59c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b59c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b59c-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a><span data-ttu-id="2b59c-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2b59c-110">Property value</span></span>

<span data-ttu-id="2b59c-111">Instância de [**monoitem**](counteritem.md) que corresponde ao valor de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2b59c-111">[**CounterItem**](counteritem.md) instance that corresponds to the specified index value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="2b59c-112">Exceções</span><span class="sxs-lookup"><span data-stu-id="2b59c-112">Exceptions</span></span>



| <span data-ttu-id="2b59c-113">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="2b59c-113">Exception type</span></span>                                  | <span data-ttu-id="2b59c-114">Condição</span><span class="sxs-lookup"><span data-stu-id="2b59c-114">Condition</span></span>                         |
|-------------------------------------------------|-----------------------------------|
| <span data-ttu-id="2b59c-115">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="2b59c-115">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="2b59c-116">O índice especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="2b59c-116">The specified index is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2b59c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b59c-117">Remarks</span></span>

<span data-ttu-id="2b59c-118">Essa é a propriedade padrão do objeto [**Counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="2b59c-118">This is the default property of the [**Counters**](counters.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b59c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b59c-119">Requirements</span></span>



| <span data-ttu-id="2b59c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b59c-120">Requirement</span></span> | <span data-ttu-id="2b59c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2b59c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b59c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b59c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b59c-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2b59c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2b59c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b59c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b59c-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2b59c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b59c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2b59c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b59c-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2b59c-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b59c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b59c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b59c-129">**Item**</span><span class="sxs-lookup"><span data-stu-id="2b59c-129">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="2b59c-130">**Contadores**</span><span class="sxs-lookup"><span data-stu-id="2b59c-130">**Counters**</span></span>](counters.md)
</dt> </dl>

 

 





