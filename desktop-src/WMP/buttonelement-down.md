---
title: BOTÃO. para baixo
description: O atributo down especifica ou recupera um valor que indica se o elemento Button está na posição para cima ou para baixo.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONelement. inoperante do Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762097"
---
# <a name="buttonelementdown"></a><span data-ttu-id="1f372-104">BOTÃO. para baixo</span><span class="sxs-lookup"><span data-stu-id="1f372-104">BUTTONELEMENT.down</span></span>

<span data-ttu-id="1f372-105">O atributo **down** especifica ou recupera um valor que indica se o elemento Button está na posição para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="1f372-105">The **down** attribute specifies or retrieves a value indicating whether the button element is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="1f372-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="1f372-106">Possible Values</span></span>

<span data-ttu-id="1f372-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1f372-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="1f372-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1f372-108">Value</span></span> | <span data-ttu-id="1f372-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f372-109">Description</span></span>                                                     |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="1f372-110">true</span><span class="sxs-lookup"><span data-stu-id="1f372-110">true</span></span>  | <span data-ttu-id="1f372-111">Indica que o **buttonelement** está na posição para baixo.</span><span class="sxs-lookup"><span data-stu-id="1f372-111">Indicates the **BUTTONELEMENT** is in the down position.</span></span>        |
| <span data-ttu-id="1f372-112">false</span><span class="sxs-lookup"><span data-stu-id="1f372-112">false</span></span> | <span data-ttu-id="1f372-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="1f372-113">Default.</span></span> <span data-ttu-id="1f372-114">Indica que o **buttonelement** está na posição para cima.</span><span class="sxs-lookup"><span data-stu-id="1f372-114">Indicates the **BUTTONELEMENT** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1f372-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f372-115">Remarks</span></span>

<span data-ttu-id="1f372-116">Para que um elemento de botão permaneça na posição inativa, **adesivo** deve ser definido como true.</span><span class="sxs-lookup"><span data-stu-id="1f372-116">For a button element to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="1f372-117">Por padrão, **adesivo** é false e qualquer tentativa **de definir como** true será ignorada.</span><span class="sxs-lookup"><span data-stu-id="1f372-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="1f372-118">Se um valor inválido for especificado, o estado anterior será mantido.</span><span class="sxs-lookup"><span data-stu-id="1f372-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f372-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f372-119">Requirements</span></span>



| <span data-ttu-id="1f372-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f372-120">Requirement</span></span> | <span data-ttu-id="1f372-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1f372-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1f372-122">Versão</span><span class="sxs-lookup"><span data-stu-id="1f372-122">Version</span></span><br/> | <span data-ttu-id="1f372-123">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1f372-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f372-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f372-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f372-125">**Elemento BUTTONelement**</span><span class="sxs-lookup"><span data-stu-id="1f372-125">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="1f372-126">**BUTTONelement. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="1f372-126">**BUTTONELEMENT.downToolTip**</span></span>](buttonelement-downtooltip.md)
</dt> </dl>

 

 





