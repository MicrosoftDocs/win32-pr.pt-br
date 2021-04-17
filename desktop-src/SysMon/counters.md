---
title: Coleção de contadores (Isysmon. h)
description: Use essa classe para gerenciar a coleção de objetos de comitem. Para recuperar esse objeto, chame SystemMonitor. Counters.
ms.assetid: 01542569-3fee-440a-8722-db377380b73c
keywords:
- Coleção de contadores SysMon
- Coleção de contadores SysMon, descrita
topic_type:
- apiref
api_name:
- Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbf8da93f13dce2ce2a290adeab9394ee8addb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749186"
---
# <a name="counters-collection"></a><span data-ttu-id="5cc1d-106">Coleção de contadores</span><span class="sxs-lookup"><span data-stu-id="5cc1d-106">Counters collection</span></span>

<span data-ttu-id="5cc1d-107">Use essa classe para gerenciar a coleção de objetos de [**comitem**](counteritem.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc1d-107">Use this class to manage the collection of [**CounterItem**](counteritem.md) objects.</span></span>

<span data-ttu-id="5cc1d-108">Para recuperar esse objeto, chame [**SystemMonitor. Counters**](systemmonitor-counters.md).</span><span class="sxs-lookup"><span data-stu-id="5cc1d-108">To retrieve this object, call [**SystemMonitor.Counters**](systemmonitor-counters.md).</span></span>

## <a name="members"></a><span data-ttu-id="5cc1d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="5cc1d-109">Members</span></span>

<span data-ttu-id="5cc1d-110">A coleção de **contadores** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5cc1d-110">The **Counters** collection has these types of members:</span></span>

-   [<span data-ttu-id="5cc1d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5cc1d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="5cc1d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5cc1d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5cc1d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5cc1d-113">Methods</span></span>

<span data-ttu-id="5cc1d-114">A coleção de **contadores** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5cc1d-114">The **Counters** collection has these methods.</span></span>



| <span data-ttu-id="5cc1d-115">Método</span><span class="sxs-lookup"><span data-stu-id="5cc1d-115">Method</span></span>                            | <span data-ttu-id="5cc1d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cc1d-116">Description</span></span>                                                                           |
|:----------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cc1d-117">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="5cc1d-117">**Add**</span></span>](counters-add.md)       | <span data-ttu-id="5cc1d-118">Adiciona uma instância de [**monoitem**](counteritem.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="5cc1d-118">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="5cc1d-119">**Remover**</span><span class="sxs-lookup"><span data-stu-id="5cc1d-119">**Remove**</span></span>](counters-remove.md) | <span data-ttu-id="5cc1d-120">Remove uma instância de [**monoitem**](counteritem.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="5cc1d-120">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5cc1d-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5cc1d-121">Properties</span></span>

<span data-ttu-id="5cc1d-122">A coleção de **contadores** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5cc1d-122">The **Counters** collection has these properties.</span></span>



| <span data-ttu-id="5cc1d-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5cc1d-123">Property</span></span>                                   | <span data-ttu-id="5cc1d-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cc1d-124">Description</span></span>                                                                                         |
|:-------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cc1d-125">**Contar**</span><span class="sxs-lookup"><span data-stu-id="5cc1d-125">**Count**</span></span>](counters-count.md)<br/> | <span data-ttu-id="5cc1d-126">Recupera o número de instâncias de [**monoitem**](counteritem.md) na coleção.</span><span class="sxs-lookup"><span data-stu-id="5cc1d-126">Retrieves the number of [**CounterItem**](counteritem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="5cc1d-127">**Item**</span><span class="sxs-lookup"><span data-stu-id="5cc1d-127">**Item**</span></span>](counters-item.md)<br/>   | <span data-ttu-id="5cc1d-128">Recupera a instância de [**monoitem**](counteritem.md) especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="5cc1d-128">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5cc1d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cc1d-129">Remarks</span></span>

<span data-ttu-id="5cc1d-130">O objeto **Counters** é a propriedade padrão do objeto [**SystemMonitor**](systemmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc1d-130">The **Counters** object is the default property of the [**SystemMonitor**](systemmonitor.md) object.</span></span>

<span data-ttu-id="5cc1d-131">Adicione a essa coleção os contadores que você deseja grafar.</span><span class="sxs-lookup"><span data-stu-id="5cc1d-131">Add to this collection those counters that you want to graph.</span></span> <span data-ttu-id="5cc1d-132">O SYSMON recupera os valores do contador do sistema ou de um arquivo de log, dependendo da [**fonte de dados**](systemmonitor-datasourcetype.md) que você especificar.</span><span class="sxs-lookup"><span data-stu-id="5cc1d-132">SYSMON retrieves the counter values either from the system or from a log file depending on the [**data source**](systemmonitor-datasourcetype.md) that you specify.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc1d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cc1d-133">Requirements</span></span>



| <span data-ttu-id="5cc1d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cc1d-134">Requirement</span></span> | <span data-ttu-id="5cc1d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5cc1d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cc1d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cc1d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5cc1d-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5cc1d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5cc1d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5cc1d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5cc1d-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5cc1d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cc1d-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5cc1d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cc1d-141"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc1d-141"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5cc1d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5cc1d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cc1d-143"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5cc1d-143"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





