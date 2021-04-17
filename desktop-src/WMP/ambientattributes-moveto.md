---
title: Ambienteattributes. moveTo
description: O método moveTo move o controle para um novo local em uma velocidade linear.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- Windows Media Player de ambiente. moveTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794530"
---
# <a name="ambientattributesmoveto"></a><span data-ttu-id="46991-104">Ambienteattributes. moveTo</span><span class="sxs-lookup"><span data-stu-id="46991-104">AmbientAttributes.moveTo</span></span>

<span data-ttu-id="46991-105">O método **MoveTo** move o controle para um novo local em uma velocidade linear.</span><span class="sxs-lookup"><span data-stu-id="46991-105">The **moveTo** method moves the control to a new location at a linear speed.</span></span>

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a><span data-ttu-id="46991-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46991-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46991-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span><span class="sxs-lookup"><span data-stu-id="46991-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span></span>
</dt> <dd>

<span data-ttu-id="46991-108">**Número** (**longo**) especificando o novo valor para o atributo **esquerdo** do controle.</span><span class="sxs-lookup"><span data-stu-id="46991-108">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="46991-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span><span class="sxs-lookup"><span data-stu-id="46991-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span></span>
</dt> <dd>

<span data-ttu-id="46991-110">**Número** (**longo**) especificando o novo valor para o atributo **superior** do controle.</span><span class="sxs-lookup"><span data-stu-id="46991-110">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="46991-111"><span id="time"></span><span id="TIME"></span>*momento*</span><span class="sxs-lookup"><span data-stu-id="46991-111"><span id="time"></span><span id="TIME"></span>*time*</span></span>
</dt> <dd>

<span data-ttu-id="46991-112">**Número** (**longo**) que especifica o tempo, em milissegundos, que leva para que o controle seja movido para o novo local.</span><span class="sxs-lookup"><span data-stu-id="46991-112">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46991-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="46991-113">Return Value</span></span>

<span data-ttu-id="46991-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="46991-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46991-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="46991-115">Remarks</span></span>

<span data-ttu-id="46991-116">Esse método é útil para elementos de **subexibição** animados (por exemplo, se o usuário clicar em uma bandeja e os controles deslizarem).</span><span class="sxs-lookup"><span data-stu-id="46991-116">This method is useful for animated **SUBVIEW** elements (for example, if the user clicks a tray and the controls slide down).</span></span>

<span data-ttu-id="46991-117">Esse método cria um movimento linear ao mover o controle.</span><span class="sxs-lookup"><span data-stu-id="46991-117">This method creates a linear motion when moving the control.</span></span> <span data-ttu-id="46991-118">Isso é diferente de **slideto**, que cria um movimento não linear.</span><span class="sxs-lookup"><span data-stu-id="46991-118">This differs from **slideTo**, which creates a non-linear motion.</span></span>

## <a name="requirements"></a><span data-ttu-id="46991-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46991-119">Requirements</span></span>



| <span data-ttu-id="46991-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="46991-120">Requirement</span></span> | <span data-ttu-id="46991-121">Valor</span><span class="sxs-lookup"><span data-stu-id="46991-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="46991-122">Versão</span><span class="sxs-lookup"><span data-stu-id="46991-122">Version</span></span><br/> | <span data-ttu-id="46991-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="46991-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46991-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="46991-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46991-125">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="46991-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="46991-126">**Ambienteattributes. esquerda**</span><span class="sxs-lookup"><span data-stu-id="46991-126">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="46991-127">**Ambienteattributes. deslizeto**</span><span class="sxs-lookup"><span data-stu-id="46991-127">**AmbientAttributes.slideTo**</span></span>](ambientattributes-slideto.md)
</dt> <dt>

[<span data-ttu-id="46991-128">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="46991-128">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





