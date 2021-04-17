---
title: BUTTONelement. adesivo
description: O atributo adesivo especifica ou recupera um valor que indica se o BUTTONelement é uma alternância, ou seja, se é um botão de dois Estados ou de estado único.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONelement. adesivo do Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762096"
---
# <a name="buttonelementsticky"></a><span data-ttu-id="e1a19-104">BUTTONelement. adesivo</span><span class="sxs-lookup"><span data-stu-id="e1a19-104">BUTTONELEMENT.sticky</span></span>

<span data-ttu-id="e1a19-105">O atributo **adesivo** especifica ou recupera um valor que indica se o **buttonelement** é uma alternância, ou seja, se é um botão de dois Estados ou de estado único.</span><span class="sxs-lookup"><span data-stu-id="e1a19-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTONELEMENT** is a toggle, that is, whether it is a two-state or single-state button.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="e1a19-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="e1a19-106">Possible Values</span></span>

<span data-ttu-id="e1a19-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e1a19-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="e1a19-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e1a19-108">Value</span></span> | <span data-ttu-id="e1a19-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1a19-109">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="e1a19-110">true</span><span class="sxs-lookup"><span data-stu-id="e1a19-110">true</span></span>  | <span data-ttu-id="e1a19-111">**Buttonelement** é adesivo.</span><span class="sxs-lookup"><span data-stu-id="e1a19-111">**BUTTONELEMENT** is sticky.</span></span>              |
| <span data-ttu-id="e1a19-112">false</span><span class="sxs-lookup"><span data-stu-id="e1a19-112">false</span></span> | <span data-ttu-id="e1a19-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="e1a19-113">Default.</span></span> <span data-ttu-id="e1a19-114">**Buttonelement** não é adesivo.</span><span class="sxs-lookup"><span data-stu-id="e1a19-114">**BUTTONELEMENT** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e1a19-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1a19-115">Remarks</span></span>

<span data-ttu-id="e1a19-116">Se o atributo **adesivo** for definido como true, o elemento Button será alterado para o estado Down quando for clicado e permanecerá nesse estado até ser clicado novamente.</span><span class="sxs-lookup"><span data-stu-id="e1a19-116">If the **sticky** attribute is set to true, the button element will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="e1a19-117">Quando o elemento Button estiver no estado down, o atributo **down** será true e a parte apropriada do grupo de botões **downImage** será exibida.</span><span class="sxs-lookup"><span data-stu-id="e1a19-117">When the button element is in the down state, the **down** attribute will be true and the appropriate portion of the button group **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1a19-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1a19-118">Requirements</span></span>



| <span data-ttu-id="e1a19-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1a19-119">Requirement</span></span> | <span data-ttu-id="e1a19-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e1a19-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e1a19-121">Versão</span><span class="sxs-lookup"><span data-stu-id="e1a19-121">Version</span></span><br/> | <span data-ttu-id="e1a19-122">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e1a19-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1a19-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1a19-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1a19-124">**Elemento BUTTONelement**</span><span class="sxs-lookup"><span data-stu-id="e1a19-124">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="e1a19-125">**BOTÃO. para baixo**</span><span class="sxs-lookup"><span data-stu-id="e1a19-125">**BUTTONELEMENT.down**</span></span>](buttonelement-down.md)
</dt> <dt>

[<span data-ttu-id="e1a19-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="e1a19-126">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> </dl>

 

 





