---
title: THEME. openViewRelative
description: O método openViewRelative abre uma exibição em uma nova janela em uma posição inicial especificada em relação ao canto superior esquerdo da capa.
ms.assetid: fc31a1ce-e6b9-4084-b244-28fad486f485
keywords:
- THEME. openViewRelative Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openViewRelative
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80ec93055535640b84c33dde2b61ee59cd5bfdcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768621"
---
# <a name="themeopenviewrelative"></a><span data-ttu-id="e178b-104">THEME. openViewRelative</span><span class="sxs-lookup"><span data-stu-id="e178b-104">THEME.openViewRelative</span></span>

<span data-ttu-id="e178b-105">O método **openViewRelative** abre uma **exibição** em uma nova janela em uma posição inicial especificada em relação ao canto superior esquerdo da capa.</span><span class="sxs-lookup"><span data-stu-id="e178b-105">The **openViewRelative** method opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span>

``` syntax
        theme.openView(view, left, top)
```

## <a name="parameters"></a><span data-ttu-id="e178b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e178b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e178b-107"><span id="view"></span><span id="VIEW"></span>*exibição*</span><span class="sxs-lookup"><span data-stu-id="e178b-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="e178b-108">Uma **cadeia de caracteres** que especifica a **ID** da **exibição** a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="e178b-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> <dt>

<span data-ttu-id="e178b-109"><span id="left"></span><span id="LEFT"></span>*mantida*</span><span class="sxs-lookup"><span data-stu-id="e178b-109"><span id="left"></span><span id="LEFT"></span>*left*</span></span>
</dt> <dd>

<span data-ttu-id="e178b-110">Um **número** (**longo**) que especifica a distância inicial em pixels da borda esquerda da **exibição** a partir da borda esquerda da capa.</span><span class="sxs-lookup"><span data-stu-id="e178b-110">A **Number** (**long**) specifying the initial distance in pixels of the left border of the **VIEW** from the left border of the skin.</span></span> <span data-ttu-id="e178b-111">Um valor negativo indica uma posição inicial à esquerda da borda da capa.</span><span class="sxs-lookup"><span data-stu-id="e178b-111">A negative value indicates an initial position to the left of the skin border.</span></span>

</dd> <dt>

<span data-ttu-id="e178b-112"><span id="top"></span><span id="TOP"></span>*Início*</span><span class="sxs-lookup"><span data-stu-id="e178b-112"><span id="top"></span><span id="TOP"></span>*top*</span></span>
</dt> <dd>

<span data-ttu-id="e178b-113">Um **número** (**longo**) que especifica a posição inicial da borda superior da **exibição** em relação à borda superior da capa.</span><span class="sxs-lookup"><span data-stu-id="e178b-113">A **Number** (**long**) specifying the initial position of the top border of the **VIEW** relative to the top border of the skin.</span></span> <span data-ttu-id="e178b-114">Um valor negativo indica uma posição inicial acima da borda da capa.</span><span class="sxs-lookup"><span data-stu-id="e178b-114">A negative values indicates an initial position above the skin border.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e178b-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e178b-115">Return Value</span></span>

<span data-ttu-id="e178b-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e178b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e178b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e178b-117">Remarks</span></span>

<span data-ttu-id="e178b-118">A posição especificada para a **exibição** é usada na primeira vez que esse método é chamado, após o qual o usuário pode arrastar a **exibição** para outro local.</span><span class="sxs-lookup"><span data-stu-id="e178b-118">The position specified for the **VIEW** is used the first time this method is called, after which the user can drag the **VIEW** to another location.</span></span> <span data-ttu-id="e178b-119">A nova posição é salva e, em chamadas subsequentes, a posição mais recente é usada.</span><span class="sxs-lookup"><span data-stu-id="e178b-119">The new position is saved, and on subsequent calls, the most recent position is used.</span></span>

## <a name="examples"></a><span data-ttu-id="e178b-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e178b-120">Examples</span></span>


```JScript
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openViewRelative('newView', 50, 50)"/>
    <TEXT top="30" value="close" 
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="e178b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e178b-121">Requirements</span></span>



| <span data-ttu-id="e178b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e178b-122">Requirement</span></span> | <span data-ttu-id="e178b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e178b-123">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e178b-124">Versão</span><span class="sxs-lookup"><span data-stu-id="e178b-124">Version</span></span><br/> | <span data-ttu-id="e178b-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="e178b-125">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e178b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e178b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e178b-127">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="e178b-127">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="e178b-128">**THEME. closeView**</span><span class="sxs-lookup"><span data-stu-id="e178b-128">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="e178b-129">**THEME. openView**</span><span class="sxs-lookup"><span data-stu-id="e178b-129">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





