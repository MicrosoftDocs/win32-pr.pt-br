---
title: LISTBOX. popUp
description: O atributo popUp especifica um valor que indica se o elemento representa um controle de caixa de listagem ou pop-up.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX. popUp do Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813368"
---
# <a name="listboxpopup"></a><span data-ttu-id="eb67b-104">LISTBOX. popUp</span><span class="sxs-lookup"><span data-stu-id="eb67b-104">LISTBOX.popUp</span></span>

<span data-ttu-id="eb67b-105">O atributo **popUp** especifica um valor que indica se o elemento representa um controle de caixa de listagem ou pop-up.</span><span class="sxs-lookup"><span data-stu-id="eb67b-105">The **popUp** attribute specifies a value indicating whether the element represents a popup or list box control.</span></span>

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a><span data-ttu-id="eb67b-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="eb67b-106">Possible Values</span></span>

<span data-ttu-id="eb67b-107">Esse atributo é um **booliano** especificado somente no momento do design.</span><span class="sxs-lookup"><span data-stu-id="eb67b-107">This attribute is a **Boolean** specified at design time only.</span></span>



| <span data-ttu-id="eb67b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="eb67b-108">Value</span></span> | <span data-ttu-id="eb67b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb67b-109">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="eb67b-110">true</span><span class="sxs-lookup"><span data-stu-id="eb67b-110">true</span></span>  | <span data-ttu-id="eb67b-111">O elemento representa um controle Popup.</span><span class="sxs-lookup"><span data-stu-id="eb67b-111">The element represents a popup control.</span></span>    |
| <span data-ttu-id="eb67b-112">false</span><span class="sxs-lookup"><span data-stu-id="eb67b-112">false</span></span> | <span data-ttu-id="eb67b-113">O elemento representa um controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="eb67b-113">The element represents a list box control.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eb67b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb67b-114">Remarks</span></span>

<span data-ttu-id="eb67b-115">O elemento **Popup** representa um controle de caixa de listagem que é exibido somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="eb67b-115">The **POPUP** element represents a list box control that is displayed only when needed.</span></span> <span data-ttu-id="eb67b-116">É idêntico ao elemento **ListBox** , exceto pelo valor padrão desse atributo, que altera o comportamento de exibição.</span><span class="sxs-lookup"><span data-stu-id="eb67b-116">It is identical to the **LISTBOX** element except for the default value of this attribute, which changes the display behavior.</span></span> <span data-ttu-id="eb67b-117">Para elementos **ListBox** , o valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="eb67b-117">For **LISTBOX** elements, the default value is false.</span></span> <span data-ttu-id="eb67b-118">Para elementos **Popup** , o valor padrão é true.</span><span class="sxs-lookup"><span data-stu-id="eb67b-118">For **POPUP** elements, the default value is true.</span></span> <span data-ttu-id="eb67b-119">Em vez de especificar esse atributo, o elemento **ListBox** ou **Popup** deve ser usado de acordo com o comportamento desejado.</span><span class="sxs-lookup"><span data-stu-id="eb67b-119">Instead of specifying this attribute, the **LISTBOX** or **POPUP** element should be used to according to the desired behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb67b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb67b-120">Requirements</span></span>



| <span data-ttu-id="eb67b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb67b-121">Requirement</span></span> | <span data-ttu-id="eb67b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eb67b-122">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="eb67b-123">Versão</span><span class="sxs-lookup"><span data-stu-id="eb67b-123">Version</span></span><br/> | <span data-ttu-id="eb67b-124">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="eb67b-124">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb67b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb67b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb67b-126">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="eb67b-126">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="eb67b-127">**Elemento POPUP**</span><span class="sxs-lookup"><span data-stu-id="eb67b-127">**POPUP Element**</span></span>](popup-element.md)
</dt> </dl>

 

 





