---
title: Propriedade SystemMonitor. Appearance
description: Recupera ou define a aparência do controle para incluir ou omitir os efeitos de exibição tridimensionais.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Propriedade Appearance SysMon
- Propriedade Appearance SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756121"
---
# <a name="systemmonitorappearance-property"></a><span data-ttu-id="ad487-106">Propriedade SystemMonitor. Appearance</span><span class="sxs-lookup"><span data-stu-id="ad487-106">SystemMonitor.Appearance property</span></span>

<span data-ttu-id="ad487-107">Recupera ou define a aparência do controle para incluir ou omitir os efeitos de exibição tridimensionais.</span><span class="sxs-lookup"><span data-stu-id="ad487-107">Retrieves or sets the control's appearance to include or omit three-dimensional display effects.</span></span>

<span data-ttu-id="ad487-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ad487-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad487-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad487-109">Syntax</span></span>


```VB
Property Appearance As Long
```



## <a name="property-value"></a><span data-ttu-id="ad487-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ad487-110">Property value</span></span>

<span data-ttu-id="ad487-111">O valor de aparência que determina se o controle é pintado com efeitos tridimensionais.</span><span class="sxs-lookup"><span data-stu-id="ad487-111">Appearance value that determines if the control is painted with three-dimensional effects.</span></span>

<span data-ttu-id="ad487-112">Você pode definir essa propriedade como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ad487-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="ad487-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ad487-113">Value</span></span>                                                                        | <span data-ttu-id="ad487-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ad487-114">Meaning</span></span>                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad487-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ad487-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="ad487-116">Pinta o controle sem efeitos visuais.</span><span class="sxs-lookup"><span data-stu-id="ad487-116">Paints the control without visual effects.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ad487-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ad487-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ad487-118">Pinta o controle com efeitos tridimensionais.</span><span class="sxs-lookup"><span data-stu-id="ad487-118">Paints the control with three-dimensional effects.</span></span> <span data-ttu-id="ad487-119">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="ad487-119">This is the default value.</span></span><br/> |



 

## <a name="exceptions"></a><span data-ttu-id="ad487-120">Exceções</span><span class="sxs-lookup"><span data-stu-id="ad487-120">Exceptions</span></span>



| <span data-ttu-id="ad487-121">Tipo de exceção</span><span class="sxs-lookup"><span data-stu-id="ad487-121">Exception type</span></span>               | <span data-ttu-id="ad487-122">Condição</span><span class="sxs-lookup"><span data-stu-id="ad487-122">Condition</span></span>                                    |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="ad487-123">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="ad487-123">**System.ArgumentException**</span></span> | <span data-ttu-id="ad487-124">O valor de aparência especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ad487-124">The specified appearance value is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ad487-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad487-125">Remarks</span></span>

<span data-ttu-id="ad487-126">Essa é uma propriedade de ambiente.</span><span class="sxs-lookup"><span data-stu-id="ad487-126">This is an ambient property.</span></span> <span data-ttu-id="ad487-127">O valor dessa propriedade é determinado pelo contêiner.</span><span class="sxs-lookup"><span data-stu-id="ad487-127">The value of this property is determined by the container.</span></span> <span data-ttu-id="ad487-128">Definir o valor dessa propriedade pode afetar a ilusão do controle e do contêiner sendo um único aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad487-128">Setting the value of this property could affect the illusion of the control and container being a single application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad487-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad487-129">Requirements</span></span>



| <span data-ttu-id="ad487-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad487-130">Requirement</span></span> | <span data-ttu-id="ad487-131">Valor</span><span class="sxs-lookup"><span data-stu-id="ad487-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad487-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad487-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ad487-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ad487-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ad487-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad487-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ad487-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ad487-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad487-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ad487-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad487-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="ad487-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad487-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad487-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad487-139">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="ad487-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





