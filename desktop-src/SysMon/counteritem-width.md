---
title: Propriedade MyItem. Width
description: Recupera ou define a largura da linha usada para grafar o valor do contador.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Propriedade Width SysMon
- Propriedade Width SysMon, classe de coitem
- Classe monoitem SysMon, Propriedade Width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644721"
---
# <a name="counteritemwidth-property"></a><span data-ttu-id="307db-106">Propriedade MyItem. Width</span><span class="sxs-lookup"><span data-stu-id="307db-106">CounterItem.Width property</span></span>

<span data-ttu-id="307db-107">Recupera ou define a largura da linha usada para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="307db-107">Retrieves or sets the line width used to graph the counter value.</span></span>

<span data-ttu-id="307db-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="307db-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="307db-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="307db-109">Syntax</span></span>


```VB
Property Width As Long
```



## <a name="property-value"></a><span data-ttu-id="307db-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="307db-110">Property value</span></span>

<span data-ttu-id="307db-111">Largura da linha usada em um gráfico de linhas.</span><span class="sxs-lookup"><span data-stu-id="307db-111">Line width used in a line graph.</span></span> <span data-ttu-id="307db-112">Os valores válidos variam de 1 a 3, em que 1 (o valor padrão) é a largura mais estreita.</span><span class="sxs-lookup"><span data-stu-id="307db-112">Valid values range from 1 to 3, where 1 (the default value) is the narrowest width.</span></span>

<span data-ttu-id="307db-113">**Antes do Windows Vista:** Os valores válidos variam de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="307db-113">**Prior to Windows Vista:** Valid values range from 1 to 9.</span></span> <span data-ttu-id="307db-114">Não use um valor de largura maior que 3 se seu aplicativo for executado no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="307db-114">Do not use a width value greater than 3 if your application will be run on Windows Vista.</span></span>

## <a name="exceptions"></a><span data-ttu-id="307db-115">Exceções</span><span class="sxs-lookup"><span data-stu-id="307db-115">Exceptions</span></span>



| <span data-ttu-id="307db-116">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="307db-116">Exception type</span></span>               | <span data-ttu-id="307db-117">Condição</span><span class="sxs-lookup"><span data-stu-id="307db-117">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="307db-118">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="307db-118">**System.ArgumentException**</span></span> | <span data-ttu-id="307db-119">A largura da linha especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="307db-119">The specified line width is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="307db-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="307db-120">Remarks</span></span>

<span data-ttu-id="307db-121">A largura de linha padrão para os primeiros dezesseis contadores que você adiciona é 1.</span><span class="sxs-lookup"><span data-stu-id="307db-121">The default line width for the first sixteen counters that you add is 1.</span></span> <span data-ttu-id="307db-122">A largura de linha padrão para os próximos dezesseis contadores (contadores 17-32) que você adiciona é 2.</span><span class="sxs-lookup"><span data-stu-id="307db-122">The default line width for the next sixteen counters (counters 17 - 32) that you add is 2.</span></span> <span data-ttu-id="307db-123">A largura de linha padrão para os próximos dezesseis contadores (contadores 33-48) que você adiciona é 3.</span><span class="sxs-lookup"><span data-stu-id="307db-123">The default line width for the next sixteen counters (counters 33 - 48) that you add is 3.</span></span> <span data-ttu-id="307db-124">Depois disso, o SYSMON escolhe aleatoriamente a largura da linha.</span><span class="sxs-lookup"><span data-stu-id="307db-124">After that, SYSMON randomly chooses the line width.</span></span> <span data-ttu-id="307db-125">Para obter detalhes, consulte [**MyItem. Color**](counteritem-color.md).</span><span class="sxs-lookup"><span data-stu-id="307db-125">For details, see [**CounterItem.Color**](counteritem-color.md).</span></span>

<span data-ttu-id="307db-126">Para especificar um [**estilo de linha**](counteritem-linestyle.md) diferente de sólido, a largura deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="307db-126">To specify a [**line style**](counteritem-linestyle.md) other than solid, the width must be 1.</span></span> <span data-ttu-id="307db-127">Se você especificar um valor maior que 1 e especificar um estilo de linha não sólido, o SYSMON ignorará a largura da linha especificada.</span><span class="sxs-lookup"><span data-stu-id="307db-127">If you specify a value greater than 1 and specify a non-solid line style, SYSMON ignores the specified line width.</span></span>

## <a name="requirements"></a><span data-ttu-id="307db-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="307db-128">Requirements</span></span>



| <span data-ttu-id="307db-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="307db-129">Requirement</span></span> | <span data-ttu-id="307db-130">Valor</span><span class="sxs-lookup"><span data-stu-id="307db-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="307db-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="307db-131">Minimum supported client</span></span><br/> | <span data-ttu-id="307db-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="307db-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="307db-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="307db-133">Minimum supported server</span></span><br/> | <span data-ttu-id="307db-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="307db-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="307db-135">DLL</span><span class="sxs-lookup"><span data-stu-id="307db-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="307db-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="307db-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="307db-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="307db-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="307db-138">**Item**</span><span class="sxs-lookup"><span data-stu-id="307db-138">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





