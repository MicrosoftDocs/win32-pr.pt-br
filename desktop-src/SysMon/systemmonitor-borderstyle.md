---
title: Propriedade SystemMonitor. BorderStyle
description: Recupera ou define o estilo de borda do controle.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Propriedade BorderStyle SysMon
- Propriedade BorderStyle SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824358"
---
# <a name="systemmonitorborderstyle-property"></a><span data-ttu-id="32510-106">Propriedade SystemMonitor. BorderStyle</span><span class="sxs-lookup"><span data-stu-id="32510-106">SystemMonitor.BorderStyle property</span></span>

<span data-ttu-id="32510-107">Recupera ou define o estilo de borda do controle.</span><span class="sxs-lookup"><span data-stu-id="32510-107">Retrieves or sets the border style of the control.</span></span>

<span data-ttu-id="32510-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="32510-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="32510-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32510-109">Syntax</span></span>


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="32510-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="32510-110">Property value</span></span>

<span data-ttu-id="32510-111">Estilo de borda do controle.</span><span class="sxs-lookup"><span data-stu-id="32510-111">Border style of the control.</span></span>

<span data-ttu-id="32510-112">Você pode definir essa propriedade como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="32510-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="32510-113">Valor</span><span class="sxs-lookup"><span data-stu-id="32510-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="32510-114">Significado</span><span class="sxs-lookup"><span data-stu-id="32510-114">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <span data-ttu-id="32510-115"><dt>**System. Windows. Forms. FormBorderStyle. VbBSNone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="32510-115"><dt>**System.Windows.Forms.FormBorderStyle.VbBSNone**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="32510-116">Sem borda.</span><span class="sxs-lookup"><span data-stu-id="32510-116">No border.</span></span> <span data-ttu-id="32510-117">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="32510-117">This is the default value.</span></span><br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <span data-ttu-id="32510-118"><dt>**System. Windows. Forms. FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="32510-118"><dt>**System.Windows.Forms.FormBorderStyle.VbFixedSingle**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="32510-119">Fixo, borda única.</span><span class="sxs-lookup"><span data-stu-id="32510-119">Fixed, single border.</span></span><br/>                 |



 

## <a name="exceptions"></a><span data-ttu-id="32510-120">Exceções</span><span class="sxs-lookup"><span data-stu-id="32510-120">Exceptions</span></span>



| <span data-ttu-id="32510-121">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="32510-121">Exception type</span></span>               | <span data-ttu-id="32510-122">Condição</span><span class="sxs-lookup"><span data-stu-id="32510-122">Condition</span></span>                                |
|------------------------------|------------------------------------------|
| <span data-ttu-id="32510-123">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="32510-123">**System.ArgumentException**</span></span> | <span data-ttu-id="32510-124">O estilo de borda especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="32510-124">The specified border style is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="32510-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32510-125">Requirements</span></span>



| <span data-ttu-id="32510-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="32510-126">Requirement</span></span> | <span data-ttu-id="32510-127">Valor</span><span class="sxs-lookup"><span data-stu-id="32510-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32510-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32510-128">Minimum supported client</span></span><br/> | <span data-ttu-id="32510-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="32510-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="32510-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32510-130">Minimum supported server</span></span><br/> | <span data-ttu-id="32510-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="32510-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32510-132">DLL</span><span class="sxs-lookup"><span data-stu-id="32510-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32510-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="32510-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32510-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="32510-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32510-135">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="32510-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





