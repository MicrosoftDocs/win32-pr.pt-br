---
title: Ambienteattributes. deslizeto
description: O método slideto move o controle para um novo local. O controle é movido de forma não linear no período de tempo especificado.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Ambiente. Deslize para o Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761492"
---
# <a name="ambientattributesslideto"></a><span data-ttu-id="fbfec-105">Ambienteattributes. deslizeto</span><span class="sxs-lookup"><span data-stu-id="fbfec-105">AmbientAttributes.slideTo</span></span>

<span data-ttu-id="fbfec-106">O método **slideto** move o controle para um novo local.</span><span class="sxs-lookup"><span data-stu-id="fbfec-106">The **slideTo** method moves the control to a new location.</span></span> <span data-ttu-id="fbfec-107">O controle é movido de forma não linear no período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="fbfec-107">The control moves in a non-linear fashion over the specified time period.</span></span>

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a><span data-ttu-id="fbfec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbfec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbfec-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="fbfec-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="fbfec-110">**Número** (**longo**) especificando o novo valor para o atributo **esquerdo** do controle.</span><span class="sxs-lookup"><span data-stu-id="fbfec-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="fbfec-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="fbfec-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="fbfec-112">**Número** (**longo**) especificando o novo valor para o atributo **superior** do controle.</span><span class="sxs-lookup"><span data-stu-id="fbfec-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="fbfec-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*mover para*</span><span class="sxs-lookup"><span data-stu-id="fbfec-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="fbfec-114">**Número** (**longo**) que especifica o tempo, em milissegundos, que leva para que o controle seja movido para o novo local.</span><span class="sxs-lookup"><span data-stu-id="fbfec-114">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbfec-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fbfec-115">Return Value</span></span>

<span data-ttu-id="fbfec-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fbfec-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbfec-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbfec-117">Remarks</span></span>

<span data-ttu-id="fbfec-118">Esse método é diferente de **MoveTo**, que cria um movimento linear ao mover o controle.</span><span class="sxs-lookup"><span data-stu-id="fbfec-118">This method is different from **moveTo**, which creates a linear motion when moving the control.</span></span> <span data-ttu-id="fbfec-119">O movimento não linear criado por esse método é um movimento deslizante que acelera a partir de uma velocidade de zero no início do movimento e faz a desaceleração para zero no final, chegando a uma parada suave.</span><span class="sxs-lookup"><span data-stu-id="fbfec-119">The non-linear motion created by this method is a sliding motion that accelerates from a speed of zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbfec-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbfec-120">Requirements</span></span>



| <span data-ttu-id="fbfec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbfec-121">Requirement</span></span> | <span data-ttu-id="fbfec-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fbfec-122">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="fbfec-123">Versão</span><span class="sxs-lookup"><span data-stu-id="fbfec-123">Version</span></span><br/> | <span data-ttu-id="fbfec-124">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="fbfec-124">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbfec-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbfec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbfec-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="fbfec-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="fbfec-127">**Ambienteattributes. esquerda**</span><span class="sxs-lookup"><span data-stu-id="fbfec-127">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="fbfec-128">**Ambienteattributes. moveTo**</span><span class="sxs-lookup"><span data-stu-id="fbfec-128">**AmbientAttributes.moveTo**</span></span>](ambientattributes-moveto.md)
</dt> <dt>

[<span data-ttu-id="fbfec-129">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="fbfec-129">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





