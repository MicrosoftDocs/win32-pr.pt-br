---
title: Ambienteattributes. horizontalAlignment
description: O atributo horizontalAlignment especifica ou recupera um valor que indica o posicionamento horizontal do controle quando a exibição ou a subexibição pai é redimensionada.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Windows Media Player de ambiente. horizontalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761124"
---
# <a name="ambientattributeshorizontalalignment"></a><span data-ttu-id="1767a-104">Ambienteattributes. horizontalAlignment</span><span class="sxs-lookup"><span data-stu-id="1767a-104">AmbientAttributes.horizontalAlignment</span></span>

<span data-ttu-id="1767a-105">O atributo **horizontalAlignment** especifica ou recupera um valor que indica o posicionamento horizontal do controle quando a **exibição** ou a **subexibição** pai é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="1767a-105">The **horizontalAlignment** attribute specifies or retrieves a value that indicates the horizontal placement of the control when the **VIEW** or parent **SUBVIEW** is resized.</span></span>

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="1767a-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="1767a-106">Possible Values</span></span>

<span data-ttu-id="1767a-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1767a-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="1767a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1767a-108">Value</span></span>   | <span data-ttu-id="1767a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1767a-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1767a-110">esquerda</span><span class="sxs-lookup"><span data-stu-id="1767a-110">left</span></span>    | <span data-ttu-id="1767a-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="1767a-111">Default.</span></span> <span data-ttu-id="1767a-112">Mantém o posicionamento do controle em relação à esquerda da **exibição** ou da **subexibição** pai quando a exibição é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="1767a-112">Maintains the placement of the control relative to the left of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="1767a-113">direita</span><span class="sxs-lookup"><span data-stu-id="1767a-113">right</span></span>   | <span data-ttu-id="1767a-114">Mantém o posicionamento do controle em relação à direita da **exibição** ou da **subexibição** pai quando a exibição é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="1767a-114">Maintains the placement of the control relative to the right of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="1767a-115">centro</span><span class="sxs-lookup"><span data-stu-id="1767a-115">center</span></span>  | <span data-ttu-id="1767a-116">Mantém o posicionamento do controle em relação ao centro horizontal da **exibição** ou à **subexibição** pai quando a exibição é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="1767a-116">Maintains the placement of the control relative to the horizontal center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="1767a-117">Estendi</span><span class="sxs-lookup"><span data-stu-id="1767a-117">stretch</span></span> | <span data-ttu-id="1767a-118">Mantém o posicionamento do controle em relação às margens esquerda e direita da **exibição** ou **subexibição** pai quando redimensionada.</span><span class="sxs-lookup"><span data-stu-id="1767a-118">Maintains the placement of the control relative to both the left and right margins of the **VIEW** or parent **SUBVIEW** when resized.</span></span> <span data-ttu-id="1767a-119">O controle se ajusta para se ajustar quando a **exibição** ou a **subexibição** é ampliada.</span><span class="sxs-lookup"><span data-stu-id="1767a-119">The control stretches to fit when the **VIEW** or **SUBVIEW** is stretched.</span></span> <span data-ttu-id="1767a-120">A imagem real não aumenta ou diminui, a menos que seja redimensionável, mas a área clicável aumente ou diminua se não estiver limitada por um **clippingImage**.</span><span class="sxs-lookup"><span data-stu-id="1767a-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1767a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1767a-121">Remarks</span></span>

<span data-ttu-id="1767a-122">A menos que **horizontalAlignment** esteja definido como "Center", o controle manterá sua distância original da borda especificada ou de ambas as bordas se "Stretch" for especificado e o controle for redimensionável.</span><span class="sxs-lookup"><span data-stu-id="1767a-122">Unless **horizontalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="1767a-123">Se o controle não for redimensionável e "Stretch" for especificado, a região clicável será ampliada.</span><span class="sxs-lookup"><span data-stu-id="1767a-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="1767a-124">Você pode definir qualquer combinação de **horizontalAlignment** e **verticalAlignment**.</span><span class="sxs-lookup"><span data-stu-id="1767a-124">You can set any combination of **horizontalAlignment** and **verticalAlignment**.</span></span> <span data-ttu-id="1767a-125">Por exemplo, se você quiser centralizar um controle tanto horizontal quanto verticalmente, defina horizontalAlignment = "Center" verticalAlignment = "Center".</span><span class="sxs-lookup"><span data-stu-id="1767a-125">For example, if you want to center a control both horizontally and vertically, set horizontalAlignment="center" verticalAlignment="center".</span></span>

## <a name="requirements"></a><span data-ttu-id="1767a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1767a-126">Requirements</span></span>



| <span data-ttu-id="1767a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1767a-127">Requirement</span></span> | <span data-ttu-id="1767a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1767a-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1767a-129">Versão</span><span class="sxs-lookup"><span data-stu-id="1767a-129">Version</span></span><br/> | <span data-ttu-id="1767a-130">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1767a-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1767a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1767a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1767a-132">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="1767a-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="1767a-133">**Ambiente. verticalAlignment**</span><span class="sxs-lookup"><span data-stu-id="1767a-133">**AmbientAttributes.verticalAlignment**</span></span>](ambientattributes-verticalalignment.md)
</dt> <dt>

[<span data-ttu-id="1767a-134">**Ambienteattributes. clippingImage**</span><span class="sxs-lookup"><span data-stu-id="1767a-134">**AmbientAttributes.clippingImage**</span></span>](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





