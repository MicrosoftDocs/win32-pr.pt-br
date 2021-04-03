---
title: Propriedade MyItem. Color
description: Recupera ou define a cor usada para grafar o valor do contador.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Propriedade Color SysMon
- Propriedade Color SysMon, classe monoitem
- Classe monoitem SysMon, Propriedade Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644754"
---
# <a name="counteritemcolor-property"></a><span data-ttu-id="5e5a3-106">Propriedade MyItem. Color</span><span class="sxs-lookup"><span data-stu-id="5e5a3-106">CounterItem.Color property</span></span>

<span data-ttu-id="5e5a3-107">Recupera ou define a cor usada para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-107">Retrieves or sets the color used to graph the counter value.</span></span>

<span data-ttu-id="5e5a3-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5a3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e5a3-109">Syntax</span></span>


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a><span data-ttu-id="5e5a3-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5e5a3-110">Property value</span></span>

<span data-ttu-id="5e5a3-111">A cor usada para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-111">Color used to graph the counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e5a3-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e5a3-112">Remarks</span></span>

<span data-ttu-id="5e5a3-113">Se você não especificar a cor a ser usada, o SYSMON selecionará as cores dos primeiros dezesseis contadores.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-113">If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="5e5a3-114">Se você especificar mais de dezesseis contadores, o SYSMON reutilizará as mesmas cores dos primeiros dezesseis contadores.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-114">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="5e5a3-115">Para ajudar a distinguir os contadores um do outro, o SYSMON altera o [**estilo de linha**](counteritem-linestyle.md) usado para cada múltiplo de dezesseis contadores até os primeiros 80 contadores.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-115">To help distinguish the counters from one another, SYSMON changes the [**line style**](counteritem-linestyle.md) used for each multiple of sixteen counters up to the first 80 counters.</span></span> <span data-ttu-id="5e5a3-116">Por exemplo, os primeiros dezesseis contadores usam um estilo de linha sólida, os próximos dezesseis usam um estilo de linha tracejada e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-116">For example, the first sixteen counters use a solid line style, the next sixteen use a dash line style, and so on.</span></span> <span data-ttu-id="5e5a3-117">Em seguida, o SYSMON define a [**largura da linha**](counteritem-width.md) como 2 para os contadores 81-96 e 3 para os contadores 96-112.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-117">SYSMON then sets the [**line width**](counteritem-width.md) to 2 for counters 81 - 96 and to 3 for counters 96 - 112.</span></span> <span data-ttu-id="5e5a3-118">Se a coleção contiver mais de 112 contadores, os contadores conterão valores de cor, de linha e de largura duplicados.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-118">If the collection contains more than 112 counters, the counters will contain duplicate color, line style, and width values.</span></span>

<span data-ttu-id="5e5a3-119">**Antes do Windows Vista:** Se você não especificar a cor a ser usada, o SYSMON selecionará as cores dos primeiros dezesseis contadores.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-119">**Prior to Windows Vista:** If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="5e5a3-120">Se você especificar mais de dezesseis contadores, o SYSMON reutilizará as mesmas cores dos primeiros dezesseis contadores.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-120">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="5e5a3-121">Para ajudar a distinguir os contadores um do outro, o SYSMON aumenta a [**largura da linha**](counteritem-width.md) dos três primeiros contadores que recebem a mesma atribuição de cor.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-121">To help distinguish the counters from one another, SYSMON increases the [**line width**](counteritem-width.md) of the first three counters that receive the same color assignment.</span></span> <span data-ttu-id="5e5a3-122">Se mais de três contadores usarem a mesma cor, o SYSMON escolherá aleatoriamente a largura da linha a ser usada para o contador.</span><span class="sxs-lookup"><span data-stu-id="5e5a3-122">If more than three counters use the same color, SYSMON randomly chooses the line width to use for the counter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5a3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e5a3-123">Requirements</span></span>



| <span data-ttu-id="5e5a3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e5a3-124">Requirement</span></span> | <span data-ttu-id="5e5a3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5e5a3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5a3-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5a3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5a3-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e5a3-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5e5a3-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e5a3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5a3-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e5a3-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e5a3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5e5a3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e5a3-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5e5a3-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e5a3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e5a3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5a3-133">**Item**</span><span class="sxs-lookup"><span data-stu-id="5e5a3-133">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





