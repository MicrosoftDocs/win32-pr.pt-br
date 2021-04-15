---
title: BOTÃO. para baixo
description: O atributo down especifica ou recupera um valor que indica se o botão está na posição para cima ou para baixo.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BOTÃO. abaixar o Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761481"
---
# <a name="buttondown"></a><span data-ttu-id="4eefd-104">BOTÃO. para baixo</span><span class="sxs-lookup"><span data-stu-id="4eefd-104">BUTTON.down</span></span>

<span data-ttu-id="4eefd-105">O atributo **down** especifica ou recupera um valor que indica se o **botão** está na posição para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="4eefd-105">The **down** attribute specifies or retrieves a value indicating whether the **BUTTON** is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="4eefd-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4eefd-106">Possible Values</span></span>

<span data-ttu-id="4eefd-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4eefd-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="4eefd-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4eefd-108">Value</span></span> | <span data-ttu-id="4eefd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4eefd-109">Description</span></span>                                                   |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="4eefd-110">true</span><span class="sxs-lookup"><span data-stu-id="4eefd-110">true</span></span>  | <span data-ttu-id="4eefd-111">Indica que o **botão** está na posição para baixo.</span><span class="sxs-lookup"><span data-stu-id="4eefd-111">Indicates that the **BUTTON** is in the down position.</span></span>        |
| <span data-ttu-id="4eefd-112">false</span><span class="sxs-lookup"><span data-stu-id="4eefd-112">false</span></span> | <span data-ttu-id="4eefd-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="4eefd-113">Default.</span></span> <span data-ttu-id="4eefd-114">Indica que o **botão** está na posição para cima.</span><span class="sxs-lookup"><span data-stu-id="4eefd-114">Indicates that the **BUTTON** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4eefd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4eefd-115">Remarks</span></span>

<span data-ttu-id="4eefd-116">Para que um **botão** permaneça na posição inativa, **adesivo** deve ser definido como true.</span><span class="sxs-lookup"><span data-stu-id="4eefd-116">For a **BUTTON** to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="4eefd-117">Por padrão, **adesivo** é false e qualquer tentativa **de definir como** true será ignorada.</span><span class="sxs-lookup"><span data-stu-id="4eefd-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="4eefd-118">Se um valor inválido for especificado, o estado anterior será mantido.</span><span class="sxs-lookup"><span data-stu-id="4eefd-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eefd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eefd-119">Requirements</span></span>



| <span data-ttu-id="4eefd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eefd-120">Requirement</span></span> | <span data-ttu-id="4eefd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4eefd-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4eefd-122">Versão</span><span class="sxs-lookup"><span data-stu-id="4eefd-122">Version</span></span><br/> | <span data-ttu-id="4eefd-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4eefd-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4eefd-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4eefd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eefd-125">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="4eefd-125">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="4eefd-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="4eefd-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> <dt>

[<span data-ttu-id="4eefd-127">**BUTTON. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="4eefd-127">**BUTTON.downToolTip**</span></span>](button-downtooltip.md)
</dt> </dl>

 

 





