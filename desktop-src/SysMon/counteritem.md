---
title: Objeto de coitem (Isysmon. h)
description: Use essa classe para recuperar o caminho e o valor de um contador e para especificar a cor usada para grafar o contador. Para recuperar esse objeto, chame Counters. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Objeto de coitem SysMon
- Objeto de coitem SysMon, descrito
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644753"
---
# <a name="counteritem-object"></a><span data-ttu-id="22fbe-106">Objeto de coitem</span><span class="sxs-lookup"><span data-stu-id="22fbe-106">CounterItem object</span></span>

<span data-ttu-id="22fbe-107">Use essa classe para recuperar o caminho e o valor de um contador e para especificar a cor usada para grafar o contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-107">Use this class to retrieve the path and value of a counter and to specify the color used to graph the counter.</span></span>

<span data-ttu-id="22fbe-108">Para recuperar esse objeto, chame [**Counters. Item**](counters-item.md).</span><span class="sxs-lookup"><span data-stu-id="22fbe-108">To retrieve this object, call [**Counters.Item**](counters-item.md).</span></span>

## <a name="members"></a><span data-ttu-id="22fbe-109">Membros</span><span class="sxs-lookup"><span data-stu-id="22fbe-109">Members</span></span>

<span data-ttu-id="22fbe-110">O objeto de **coitem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="22fbe-110">The **CounterItem** object has these types of members:</span></span>

-   [<span data-ttu-id="22fbe-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="22fbe-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="22fbe-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="22fbe-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22fbe-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="22fbe-113">Methods</span></span>

<span data-ttu-id="22fbe-114">O objeto de **coitem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="22fbe-114">The **CounterItem** object has these methods.</span></span>



| <span data-ttu-id="22fbe-115">Método</span><span class="sxs-lookup"><span data-stu-id="22fbe-115">Method</span></span>                                             | <span data-ttu-id="22fbe-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="22fbe-116">Description</span></span>                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="22fbe-117">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="22fbe-117">**GetDataAt**</span></span>](counteritem-getdataat.md)         | <span data-ttu-id="22fbe-118">Recupera os dados do contador de um ponto específico no gráfico de linhas.</span><span class="sxs-lookup"><span data-stu-id="22fbe-118">Retrieves the counter data from a specific point in the line graph.</span></span><br/> |
| [<span data-ttu-id="22fbe-119">**Getstatistics**</span><span class="sxs-lookup"><span data-stu-id="22fbe-119">**GetStatistics**</span></span>](counteritem-getstatistics.md) | <span data-ttu-id="22fbe-120">Recupera os valores médio, máximo e mínimo para o contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-120">Retrieves the average, maximum, and minimum values for the counter.</span></span><br/> |
| [<span data-ttu-id="22fbe-121">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="22fbe-121">**GetValue**</span></span>](counteritem-getvalue.md)           | <span data-ttu-id="22fbe-122">Recupera o último valor do contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-122">Retrieves the last value of the counter.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="22fbe-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="22fbe-123">Properties</span></span>

<span data-ttu-id="22fbe-124">O objeto de **coitem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="22fbe-124">The **CounterItem** object has these properties.</span></span>



| <span data-ttu-id="22fbe-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="22fbe-125">Property</span></span>                                                  | <span data-ttu-id="22fbe-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="22fbe-126">Description</span></span>                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="22fbe-127">**Cor**</span><span class="sxs-lookup"><span data-stu-id="22fbe-127">**Color**</span></span>](counteritem-color.md)<br/>             | <span data-ttu-id="22fbe-128">Recupera ou define a cor usada para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-128">Retrieves or sets the color used to graph the counter value.</span></span><br/>         |
| [<span data-ttu-id="22fbe-129">**Estilo de Linha**</span><span class="sxs-lookup"><span data-stu-id="22fbe-129">**LineStyle**</span></span>](counteritem-linestyle.md)<br/>     | <span data-ttu-id="22fbe-130">Recupera ou define o estilo de linha usado para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-130">Retrieves or sets the line style used to graph the counter value.</span></span><br/>    |
| [<span data-ttu-id="22fbe-131">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="22fbe-131">**Path**</span></span>](counteritem-path.md)<br/>               | <span data-ttu-id="22fbe-132">Recupera o caminho do contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-132">Retrieves the path of the counter.</span></span><br/>                                   |
| [<span data-ttu-id="22fbe-133">**ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="22fbe-133">**ScaleFactor**</span></span>](counteritem-scalefactor.md)<br/> | <span data-ttu-id="22fbe-134">Recupera ou define o fator de escala usado para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-134">Retrieves or sets the scale factor used to graph the counter value.</span></span><br/>  |
| [<span data-ttu-id="22fbe-135">**Selected**</span><span class="sxs-lookup"><span data-stu-id="22fbe-135">**Selected**</span></span>](counteritem-selected.md)<br/>       | <span data-ttu-id="22fbe-136">Recupera ou define um valor que indica se o contador está selecionado.</span><span class="sxs-lookup"><span data-stu-id="22fbe-136">Retrieves or sets a value that indicates if the counter is selected.</span></span><br/> |
| [<span data-ttu-id="22fbe-137">**Valor**</span><span class="sxs-lookup"><span data-stu-id="22fbe-137">**Value**</span></span>](counteritem-value.md)<br/>             | <span data-ttu-id="22fbe-138">Recupera o valor atual do contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-138">Retrieves the current value of the counter.</span></span><br/>                          |
| [<span data-ttu-id="22fbe-139">**Visible**</span><span class="sxs-lookup"><span data-stu-id="22fbe-139">**Visible**</span></span>](counteritem-visible.md)<br/>         | <span data-ttu-id="22fbe-140">Recupera ou define um valor que indica se o contador está grafado.</span><span class="sxs-lookup"><span data-stu-id="22fbe-140">Retrieves or sets a value that indicates if the counter is graphed.</span></span><br/>  |
| [<span data-ttu-id="22fbe-141">**Largura**</span><span class="sxs-lookup"><span data-stu-id="22fbe-141">**Width**</span></span>](counteritem-width.md)<br/>             | <span data-ttu-id="22fbe-142">Recupera ou define a largura da linha usada para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="22fbe-142">Retrieves or sets the line width used to graph the counter value.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="22fbe-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="22fbe-143">Remarks</span></span>

<span data-ttu-id="22fbe-144">O [**valor**](counteritem-value.md) é a propriedade padrão do **item de itens**.</span><span class="sxs-lookup"><span data-stu-id="22fbe-144">[**Value**](counteritem-value.md) is the default property of **CounterItem**.</span></span>

## <a name="requirements"></a><span data-ttu-id="22fbe-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22fbe-145">Requirements</span></span>



| <span data-ttu-id="22fbe-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="22fbe-146">Requirement</span></span> | <span data-ttu-id="22fbe-147">Valor</span><span class="sxs-lookup"><span data-stu-id="22fbe-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22fbe-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22fbe-148">Minimum supported client</span></span><br/> | <span data-ttu-id="22fbe-149">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22fbe-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="22fbe-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22fbe-150">Minimum supported server</span></span><br/> | <span data-ttu-id="22fbe-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22fbe-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22fbe-152">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="22fbe-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="22fbe-153"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="22fbe-153"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="22fbe-154">DLL</span><span class="sxs-lookup"><span data-stu-id="22fbe-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22fbe-155"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="22fbe-155"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22fbe-156">Consulte também</span><span class="sxs-lookup"><span data-stu-id="22fbe-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22fbe-157">Classes SYSMON</span><span class="sxs-lookup"><span data-stu-id="22fbe-157">SYSMON Classes</span></span>](sysmon-classes.md)
</dt> </dl>

 

 





