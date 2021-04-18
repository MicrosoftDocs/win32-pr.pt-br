---
title: Ambiente. verticalAlignment
description: O atributo verticalAlignment especifica ou recupera um valor que indica o posicionamento vertical do controle quando a exibição ou a subexibição pai é ampliada.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Windows Media Player de ambiente. verticalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781466"
---
# <a name="ambientattributesverticalalignment"></a><span data-ttu-id="8b611-104">Ambiente. verticalAlignment</span><span class="sxs-lookup"><span data-stu-id="8b611-104">AmbientAttributes.verticalAlignment</span></span>

<span data-ttu-id="8b611-105">O atributo **verticalAlignment** especifica ou recupera um valor que indica o posicionamento vertical do controle quando a **exibição** ou a **subexibição** pai é ampliada.</span><span class="sxs-lookup"><span data-stu-id="8b611-105">The **verticalAlignment** attribute specifies or retrieves a value indicating the vertical placement of the control when the **VIEW** or parent **SUBVIEW** is stretched.</span></span>

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a><span data-ttu-id="8b611-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="8b611-106">Possible Values</span></span>

<span data-ttu-id="8b611-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8b611-107">This attribute is a read/write **String**.</span></span>



| <span data-ttu-id="8b611-108">Valor</span><span class="sxs-lookup"><span data-stu-id="8b611-108">Value</span></span>   | <span data-ttu-id="8b611-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b611-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b611-110">top</span><span class="sxs-lookup"><span data-stu-id="8b611-110">top</span></span>     | <span data-ttu-id="8b611-111">Padrão.</span><span class="sxs-lookup"><span data-stu-id="8b611-111">Default.</span></span> <span data-ttu-id="8b611-112">Mantém o posicionamento do controle em relação à parte superior da **exibição** ou da **subexibição** pai quando a exibição é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="8b611-112">Maintains the placement of the control relative to the top of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="8b611-113">parte inferior</span><span class="sxs-lookup"><span data-stu-id="8b611-113">bottom</span></span>  | <span data-ttu-id="8b611-114">Mantém o posicionamento do controle em relação à parte inferior da **exibição** ou da **subexibição** pai quando a exibição é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="8b611-114">Maintains the placement of the control relative to the bottom of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="8b611-115">centro</span><span class="sxs-lookup"><span data-stu-id="8b611-115">center</span></span>  | <span data-ttu-id="8b611-116">Mantém o posicionamento do controle em relação ao centro vertical da **exibição** ou à **subexibição** pai quando a exibição é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="8b611-116">Maintains the placement of the control relative to the vertical center of the **VIEW** or parent **SUBVIEW** when the view is resized.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="8b611-117">Estendi</span><span class="sxs-lookup"><span data-stu-id="8b611-117">stretch</span></span> | <span data-ttu-id="8b611-118">Mantém o posicionamento do controle em relação às margens superior e inferior da exibição quando redimensionada.</span><span class="sxs-lookup"><span data-stu-id="8b611-118">Maintains the placement of the control relative to both the top and bottom margins of the View when resized.</span></span> <span data-ttu-id="8b611-119">O controle se ajusta para se ajustar quando a **exibição** ou a **subexibição** pai é ampliada.</span><span class="sxs-lookup"><span data-stu-id="8b611-119">The control stretches to fit when the **VIEW** or parent **SUBVIEW** is stretched.</span></span> <span data-ttu-id="8b611-120">A imagem real não aumenta ou diminui, a menos que seja redimensionável, mas a área clicável aumente ou diminua se não estiver limitada por um **clippingImage**.</span><span class="sxs-lookup"><span data-stu-id="8b611-120">The actual image does not grow or shrink unless it is resizable, but the clickable area grows or shrinks if not bounded by a **clippingImage**.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8b611-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b611-121">Remarks</span></span>

<span data-ttu-id="8b611-122">A menos que o **verticalAlignment** esteja definido como "Center", o controle retém sua distância original da borda especificada ou de ambas as bordas se "Stretch" for especificado e o controle for redimensionável.</span><span class="sxs-lookup"><span data-stu-id="8b611-122">Unless **verticalAlignment** is set to "center", the control retains its original distance from the specified edge, or from both edges if "stretch" is specified and the control is resizable.</span></span> <span data-ttu-id="8b611-123">Se o controle não for redimensionável e "Stretch" for especificado, a região clicável será ampliada.</span><span class="sxs-lookup"><span data-stu-id="8b611-123">If the control is not resizable and "stretch" is specified, the clickable region is stretched instead.</span></span>

<span data-ttu-id="8b611-124">Você pode definir qualquer combinação dos atributos **horizontalAlignment** e **verticalAlignment** .</span><span class="sxs-lookup"><span data-stu-id="8b611-124">You can set any combination of the **horizontalAlignment** and **verticalAlignment** attributes.</span></span> <span data-ttu-id="8b611-125">Por exemplo, se você quiser que um controle seja centralizado horizontalmente e verticalmente, defina **horizontalAlignment** como "Center" e **verticalAlignment** como "Center".</span><span class="sxs-lookup"><span data-stu-id="8b611-125">For example, if you want a control to be centered both horizontally and vertically, set **horizontalAlignment** to "center" and **verticalAlignment** to "center".</span></span>

## <a name="requirements"></a><span data-ttu-id="8b611-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b611-126">Requirements</span></span>



| <span data-ttu-id="8b611-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b611-127">Requirement</span></span> | <span data-ttu-id="8b611-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8b611-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8b611-129">Versão</span><span class="sxs-lookup"><span data-stu-id="8b611-129">Version</span></span><br/> | <span data-ttu-id="8b611-130">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8b611-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b611-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b611-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b611-132">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="8b611-132">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b611-133">**Ambienteattributes. horizontalAlignment**</span><span class="sxs-lookup"><span data-stu-id="8b611-133">**AmbientAttributes.horizontalAlignment**</span></span>](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





