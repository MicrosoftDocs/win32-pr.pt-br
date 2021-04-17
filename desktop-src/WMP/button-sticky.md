---
title: BOTÃO. adesivo
description: O atributo adesivo especifica ou recupera um valor que indica se o botão é uma alternância, ou seja, se é um botão de dois Estados ou de estado único.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BOTÃO. autoadesiva do Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813379"
---
# <a name="buttonsticky"></a><span data-ttu-id="0c610-104">BOTÃO. adesivo</span><span class="sxs-lookup"><span data-stu-id="0c610-104">BUTTON.sticky</span></span>

<span data-ttu-id="0c610-105">O atributo **adesivo** especifica ou recupera um valor que indica se o **botão** é uma alternância, ou seja, se é um **botão** de dois Estados ou de estado único.</span><span class="sxs-lookup"><span data-stu-id="0c610-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTON** is a toggle, that is, whether it is a two-state or single-state **BUTTON**.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="0c610-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0c610-106">Possible Values</span></span>

<span data-ttu-id="0c610-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0c610-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="0c610-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0c610-108">Value</span></span> | <span data-ttu-id="0c610-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c610-109">Description</span></span>                        |
|-------|------------------------------------|
| <span data-ttu-id="0c610-110">true</span><span class="sxs-lookup"><span data-stu-id="0c610-110">true</span></span>  | <span data-ttu-id="0c610-111">O **botão** é adesivo.</span><span class="sxs-lookup"><span data-stu-id="0c610-111">**BUTTON** is sticky.</span></span>              |
| <span data-ttu-id="0c610-112">false</span><span class="sxs-lookup"><span data-stu-id="0c610-112">false</span></span> | <span data-ttu-id="0c610-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="0c610-113">Default.</span></span> <span data-ttu-id="0c610-114">O **botão** não é adesivo.</span><span class="sxs-lookup"><span data-stu-id="0c610-114">**BUTTON** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0c610-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c610-115">Remarks</span></span>

<span data-ttu-id="0c610-116">Se **adesivo** estiver definido como true, o **botão** será alterado para o estado Down quando clicado e permanecerá nesse estado até que seja clicado novamente.</span><span class="sxs-lookup"><span data-stu-id="0c610-116">If **sticky** is set to true, the **BUTTON** will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="0c610-117">Quando o **botão** estiver no estado inativo, o atributo **down** será true e o **downImage** será exibido.</span><span class="sxs-lookup"><span data-stu-id="0c610-117">When the **BUTTON** is in the down state, the **down** attribute will be true and the **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c610-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c610-118">Requirements</span></span>



| <span data-ttu-id="0c610-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c610-119">Requirement</span></span> | <span data-ttu-id="0c610-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0c610-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0c610-121">Versão</span><span class="sxs-lookup"><span data-stu-id="0c610-121">Version</span></span><br/> | <span data-ttu-id="0c610-122">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="0c610-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c610-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c610-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c610-124">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="0c610-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="0c610-125">**BOTÃO. para baixo**</span><span class="sxs-lookup"><span data-stu-id="0c610-125">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="0c610-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="0c610-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





