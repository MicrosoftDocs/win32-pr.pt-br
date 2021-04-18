---
title: Ambienteattributes. moveSizeTo
description: O método moveSizeTo move o controle e especifica um novo tamanho para o controle no novo local. O controle é movido e redimensionado de maneira animada no período de tempo especificado.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- MoveSizeTo do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810591"
---
# <a name="ambientattributesmovesizeto"></a><span data-ttu-id="3ecfe-105">Ambienteattributes. moveSizeTo</span><span class="sxs-lookup"><span data-stu-id="3ecfe-105">AmbientAttributes.moveSizeTo</span></span>

<span data-ttu-id="3ecfe-106">O método **moveSizeTo** move o controle e especifica um novo tamanho para o controle no novo local.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-106">The **moveSizeTo** method moves the control and specifies a new size for the control in the new location.</span></span> <span data-ttu-id="3ecfe-107">O controle é movido e redimensionado de maneira animada no período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-107">The control moves and resizes in an animated fashion over the specified time period.</span></span>

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a><span data-ttu-id="3ecfe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ecfe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ecfe-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="3ecfe-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="3ecfe-110">**Número** (**longo**) especificando o novo valor para o atributo **esquerdo** do controle.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="3ecfe-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="3ecfe-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="3ecfe-112">**Número** (**longo**) especificando o novo valor para o atributo **superior** do controle.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="3ecfe-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span><span class="sxs-lookup"><span data-stu-id="3ecfe-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span></span>
</dt> <dd>

<span data-ttu-id="3ecfe-114">**Número** (**longo**) especificando o novo valor para o atributo de **largura** do controle.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-114">**Number** (**long**) specifying the new value for the **width** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="3ecfe-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span><span class="sxs-lookup"><span data-stu-id="3ecfe-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span></span>
</dt> <dd>

<span data-ttu-id="3ecfe-116">**Número** (**longo**) especificando o novo valor para o atributo de **altura** do controle.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-116">**Number** (**long**) specifying the new value for the **height** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="3ecfe-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*mover para*</span><span class="sxs-lookup"><span data-stu-id="3ecfe-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="3ecfe-118">**Número** (**longo**) que especifica o tempo, em milissegundos, que leva para que o controle seja movido para o novo local.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-118">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> <dt>

<span data-ttu-id="3ecfe-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span><span class="sxs-lookup"><span data-stu-id="3ecfe-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span></span>
</dt> <dd>

<span data-ttu-id="3ecfe-120">**Booliano** que especifica o tipo de movimento criado ao mover o controle.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-120">**Boolean** specifying the type of motion created when moving the control.</span></span>



| <span data-ttu-id="3ecfe-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3ecfe-121">Value</span></span> | <span data-ttu-id="3ecfe-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ecfe-122">Description</span></span>                                                             |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="3ecfe-123">true</span><span class="sxs-lookup"><span data-stu-id="3ecfe-123">true</span></span>  | <span data-ttu-id="3ecfe-124">O movimento não é linear (movimento deslizante que acelera e diminui).</span><span class="sxs-lookup"><span data-stu-id="3ecfe-124">Motion is non-linear (sliding motion that accelerates and decelerates).</span></span> |
| <span data-ttu-id="3ecfe-125">false</span><span class="sxs-lookup"><span data-stu-id="3ecfe-125">false</span></span> | <span data-ttu-id="3ecfe-126">O movimento é linear.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-126">Motion is linear.</span></span>                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ecfe-127">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3ecfe-127">Return Value</span></span>

<span data-ttu-id="3ecfe-128">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ecfe-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ecfe-129">Remarks</span></span>

<span data-ttu-id="3ecfe-130">O movimento do controle pode ser linear ou não linear.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-130">The motion of the control can be linear or non-linear.</span></span> <span data-ttu-id="3ecfe-131">Movimento linear significa que o controle se move em uma velocidade constante para seu novo local, iniciando e parando abruptamente.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-131">Linear motion means the control moves at a constant speed to its new location, starting and stopping abruptly.</span></span> <span data-ttu-id="3ecfe-132">Quando o movimento não linear é especificado, é criado um movimento deslizante que acelera de zero no início do movimento e que é reduzido de volta para zero no final, chegando a uma parada suave.</span><span class="sxs-lookup"><span data-stu-id="3ecfe-132">When non-linear motion is specified, a sliding motion is created that accelerates from zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecfe-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ecfe-133">Requirements</span></span>



| <span data-ttu-id="3ecfe-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ecfe-134">Requirement</span></span> | <span data-ttu-id="3ecfe-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3ecfe-135">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="3ecfe-136">Versão</span><span class="sxs-lookup"><span data-stu-id="3ecfe-136">Version</span></span><br/> | <span data-ttu-id="3ecfe-137">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="3ecfe-137">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ecfe-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ecfe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecfe-139">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="3ecfe-139">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ecfe-140">**Ambiente. altura**</span><span class="sxs-lookup"><span data-stu-id="3ecfe-140">**AmbientAttributes.height**</span></span>](ambientattributes-height.md)
</dt> <dt>

[<span data-ttu-id="3ecfe-141">**Ambienteattributes. esquerda**</span><span class="sxs-lookup"><span data-stu-id="3ecfe-141">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="3ecfe-142">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="3ecfe-142">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> <dt>

[<span data-ttu-id="3ecfe-143">**Ambiente. largura**</span><span class="sxs-lookup"><span data-stu-id="3ecfe-143">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> </dl>

 

 





