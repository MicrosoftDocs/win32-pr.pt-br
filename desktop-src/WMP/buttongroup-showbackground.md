---
title: BOTÃO de fundo.
description: O atributo de exibição de fundo especifica ou recupera um valor que indica se o myButton exibe apenas os botões ou exibe o bitmap completo especificado no atributo Image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- The. para o Windows Media Player em segundo plano
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796440"
---
# <a name="buttongroupshowbackground"></a><span data-ttu-id="61a7c-104">BOTÃO de fundo.</span><span class="sxs-lookup"><span data-stu-id="61a7c-104">BUTTONGROUP.showBackground</span></span>

<span data-ttu-id="61a7c-105">O atributo de exibição de **fundo** especifica ou recupera um valor que indica se o **MyButton** exibe apenas os botões ou exibe o bitmap completo especificado no atributo **Image** .</span><span class="sxs-lookup"><span data-stu-id="61a7c-105">The **showBackground** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a><span data-ttu-id="61a7c-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="61a7c-106">Possible Values</span></span>

<span data-ttu-id="61a7c-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="61a7c-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="61a7c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="61a7c-108">Value</span></span> | <span data-ttu-id="61a7c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="61a7c-109">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a7c-110">true</span><span class="sxs-lookup"><span data-stu-id="61a7c-110">true</span></span>  | <span data-ttu-id="61a7c-111">Os botões são exibidos e a área não ocupada pelos botões é desenhada a partir do bitmap de imagem.</span><span class="sxs-lookup"><span data-stu-id="61a7c-111">Buttons are displayed and the area not occupied by buttons is drawn from the Image bitmap.</span></span> |
| <span data-ttu-id="61a7c-112">false</span><span class="sxs-lookup"><span data-stu-id="61a7c-112">false</span></span> | <span data-ttu-id="61a7c-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="61a7c-113">Default.</span></span> <span data-ttu-id="61a7c-114">Somente os botões são exibidos.</span><span class="sxs-lookup"><span data-stu-id="61a7c-114">Only the buttons are displayed.</span></span>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="61a7c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="61a7c-115">Remarks</span></span>

<span data-ttu-id="61a7c-116">Quando o modo de **fundo** for true, toda a **imagem** principal ficará visível.</span><span class="sxs-lookup"><span data-stu-id="61a7c-116">When **showBackground** is true, the entire main **image** will be visible.</span></span>

<span data-ttu-id="61a7c-117">Quando a cor do **plano de fundo** for falsa, somente as áreas correspondentes às cores **mappingImage** atribuídas serão renderizadas.</span><span class="sxs-lookup"><span data-stu-id="61a7c-117">When **showBackground** is false, only the areas corresponding to assigned **mappingImage** colors will be rendered.</span></span> <span data-ttu-id="61a7c-118">Em outras palavras, somente **BUTTONELEMENTs** com seus **mappingColor** atribuídos estarão visíveis.</span><span class="sxs-lookup"><span data-stu-id="61a7c-118">In other words, only **BUTTONELEMENTs** with their **mappingColor** assigned will be visible.</span></span>

<span data-ttu-id="61a7c-119">Se um valor inválido for especificado, o estado anterior será mantido.</span><span class="sxs-lookup"><span data-stu-id="61a7c-119">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a7c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61a7c-120">Requirements</span></span>



| <span data-ttu-id="61a7c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a7c-121">Requirement</span></span> | <span data-ttu-id="61a7c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="61a7c-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="61a7c-123">Versão</span><span class="sxs-lookup"><span data-stu-id="61a7c-123">Version</span></span><br/> | <span data-ttu-id="61a7c-124">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="61a7c-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61a7c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="61a7c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a7c-126">**Elemento de botão**</span><span class="sxs-lookup"><span data-stu-id="61a7c-126">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="61a7c-127">**BUTTONelement. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="61a7c-127">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="61a7c-128">**BUTTON. Image**</span><span class="sxs-lookup"><span data-stu-id="61a7c-128">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="61a7c-129">**BUTTON. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="61a7c-129">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





