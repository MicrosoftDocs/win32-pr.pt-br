---
title: Propriedade MyItem. LineStyle
description: Recupera ou define o estilo de linha usado para grafar o valor do contador.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Propriedade LineStyle SysMon
- Propriedade LineStyle SysMon, classe de coitem
- Classe monoitem SysMon, Propriedade LineStyle
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918410"
---
# <a name="counteritemlinestyle-property"></a><span data-ttu-id="a34e7-106">Propriedade MyItem. LineStyle</span><span class="sxs-lookup"><span data-stu-id="a34e7-106">CounterItem.LineStyle property</span></span>

<span data-ttu-id="a34e7-107">Recupera ou define o estilo de linha usado para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="a34e7-107">Retrieves or sets the line style used to graph the counter value.</span></span>

<span data-ttu-id="a34e7-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a34e7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a34e7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a34e7-109">Syntax</span></span>


```VB
Property LineStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="a34e7-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a34e7-110">Property value</span></span>

<span data-ttu-id="a34e7-111">O estilo de linha usado para grafar o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="a34e7-111">The line style used to graph the counter value.</span></span> <span data-ttu-id="a34e7-112">Os valores correspondem às constantes do sistema mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a34e7-112">The values correspond to system constants shown in the following table.</span></span>



| <span data-ttu-id="a34e7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a34e7-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="a34e7-114">Significado</span><span class="sxs-lookup"><span data-stu-id="a34e7-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <span data-ttu-id="a34e7-115"><dt>**System. Drawing. Drawing2D. DashStyle. sólido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a34e7-115"><dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="a34e7-116">Linha sólida.</span><span class="sxs-lookup"><span data-stu-id="a34e7-116">Solid line.</span></span> <span data-ttu-id="a34e7-117">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="a34e7-117">This is the default value.</span></span><br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <span data-ttu-id="a34e7-118"><dt>**System. Drawing. Drawing2D. DashStyle. Dash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a34e7-118"><dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="a34e7-119">Linha pontilhada com segmentos longos e espaços estreitos.</span><span class="sxs-lookup"><span data-stu-id="a34e7-119">Dotted line with long segments and narrow spaces.</span></span><br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <span data-ttu-id="a34e7-120"><dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a34e7-120"><dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="a34e7-121">Linha pontilhada com segmentos e espaços uniformes.</span><span class="sxs-lookup"><span data-stu-id="a34e7-121">Dotted line with uniform segments and spaces.</span></span><br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <span data-ttu-id="a34e7-122"><dt>**System. Drawing. Drawing2D. DashStyle. travessão ponto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a34e7-122"><dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="a34e7-123">Linha pontilhada com segmentos curtos e longos alternados.</span><span class="sxs-lookup"><span data-stu-id="a34e7-123">Dotted line with alternating short and long segments.</span></span><br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <span data-ttu-id="a34e7-124"><dt>**System. Drawing. Drawing2D. DashStyle. travessão ponto ponto**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a34e7-124"><dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="a34e7-125">Linha pontilhada com traços alternados e pontilhados duplos.</span><span class="sxs-lookup"><span data-stu-id="a34e7-125">Dotted line with alternating dashes and double dots.</span></span><br/>  |



 

## <a name="exceptions"></a><span data-ttu-id="a34e7-126">Exceções</span><span class="sxs-lookup"><span data-stu-id="a34e7-126">Exceptions</span></span>



| <span data-ttu-id="a34e7-127">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="a34e7-127">Exception type</span></span>               | <span data-ttu-id="a34e7-128">Condição</span><span class="sxs-lookup"><span data-stu-id="a34e7-128">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="a34e7-129">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="a34e7-129">**System.ArgumentException**</span></span> | <span data-ttu-id="a34e7-130">O estilo de linha especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="a34e7-130">The specified line style is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a34e7-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="a34e7-131">Remarks</span></span>

<span data-ttu-id="a34e7-132">Para especificar um valor diferente de DashStyle. Solid, [**MyItem. Width**](counteritem-width.md) deve ser definido como 1.</span><span class="sxs-lookup"><span data-stu-id="a34e7-132">To specify a value other than DashStyle.Solid, [**CounterItem.Width**](counteritem-width.md) must be set to 1.</span></span> <span data-ttu-id="a34e7-133">Se a largura for maior que 1, o SYSMON ignorará o estilo de linha especificado e usará DashStyle. Solid.</span><span class="sxs-lookup"><span data-stu-id="a34e7-133">If the width is greater than 1, SYSMON ignores the specified line style and uses DashStyle.Solid.</span></span>

## <a name="requirements"></a><span data-ttu-id="a34e7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a34e7-134">Requirements</span></span>



| <span data-ttu-id="a34e7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a34e7-135">Requirement</span></span> | <span data-ttu-id="a34e7-136">Valor</span><span class="sxs-lookup"><span data-stu-id="a34e7-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a34e7-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a34e7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a34e7-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a34e7-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a34e7-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a34e7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a34e7-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a34e7-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a34e7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a34e7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a34e7-142"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a34e7-142"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a34e7-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a34e7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a34e7-144">**Item**</span><span class="sxs-lookup"><span data-stu-id="a34e7-144">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





