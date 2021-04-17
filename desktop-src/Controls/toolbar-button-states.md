---
title: Estados do botão da barra de ferramentas (CommCtrl. h)
description: Esta seção lista os Estados que um botão de barra de ferramentas pode ter.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749947"
---
# <a name="toolbar-button-states"></a><span data-ttu-id="57480-103">Estados de botão da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="57480-103">Toolbar Button States</span></span>

<span data-ttu-id="57480-104">Esta seção lista os Estados que um botão de barra de ferramentas pode ter.</span><span class="sxs-lookup"><span data-stu-id="57480-104">This section lists the states a toolbar button can have.</span></span>



| <span data-ttu-id="57480-105">Constante</span><span class="sxs-lookup"><span data-stu-id="57480-105">Constant</span></span>                                                                                                                                                                              | <span data-ttu-id="57480-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="57480-106">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <span data-ttu-id="57480-107"><dt>**TBSTATE \_ verificados**</dt></span><span class="sxs-lookup"><span data-stu-id="57480-107"><dt>**TBSTATE\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="57480-108">O botão tem o estilo de [**\_ verificação TBSTYLE**](toolbar-control-and-button-styles.md) e está sendo clicado.</span><span class="sxs-lookup"><span data-stu-id="57480-108">The button has the [**TBSTYLE\_CHECK**](toolbar-control-and-button-styles.md) style and is being clicked.</span></span><br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <span data-ttu-id="57480-109"><dt>**\_reticências TBSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="57480-109"><dt>**TBSTATE\_ELLIPSES**</dt></span></span> </dl>                | <span data-ttu-id="57480-110">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="57480-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="57480-111">O texto do botão é cortado e uma elipse é exibida.</span><span class="sxs-lookup"><span data-stu-id="57480-111">The button's text is cut off and an ellipsis is displayed.</span></span><br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <span data-ttu-id="57480-112"><dt>**TBSTATE \_ habilitado**</dt></span><span class="sxs-lookup"><span data-stu-id="57480-112"><dt>**TBSTATE\_ENABLED**</dt></span></span> </dl>                   | <span data-ttu-id="57480-113">O botão aceita a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="57480-113">The button accepts user input.</span></span> <span data-ttu-id="57480-114">Um botão que não tem esse estado é acinzentado.</span><span class="sxs-lookup"><span data-stu-id="57480-114">A button that does not have this state is grayed.</span></span><br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <span data-ttu-id="57480-115"><dt>**TBSTATE \_ oculto**</dt></span><span class="sxs-lookup"><span data-stu-id="57480-115"><dt>**TBSTATE\_HIDDEN**</dt></span></span> </dl>                      | <span data-ttu-id="57480-116">O botão não está visível e não pode receber entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="57480-116">The button is not visible and cannot receive user input.</span></span><br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <span data-ttu-id="57480-117"><dt>**TBSTATE \_ indeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="57480-117"><dt>**TBSTATE\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="57480-118">O botão está acinzentado.</span><span class="sxs-lookup"><span data-stu-id="57480-118">The button is grayed.</span></span><br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <span data-ttu-id="57480-119"><dt>**TBSTATE \_ marcado**</dt></span><span class="sxs-lookup"><span data-stu-id="57480-119"><dt>**TBSTATE\_MARKED**</dt></span></span> </dl>                      | <span data-ttu-id="57480-120">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="57480-120">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="57480-121">O botão é marcado.</span><span class="sxs-lookup"><span data-stu-id="57480-121">The button is marked.</span></span> <span data-ttu-id="57480-122">A interpretação de um item marcado depende do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57480-122">The interpretation of a marked item is dependent upon the application.</span></span> <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <span data-ttu-id="57480-123"><dt>**TBSTATE \_ pressionado**</dt></span><span class="sxs-lookup"><span data-stu-id="57480-123"><dt>**TBSTATE\_PRESSED**</dt></span></span> </dl>                   | <span data-ttu-id="57480-124">O botão está sendo clicado.</span><span class="sxs-lookup"><span data-stu-id="57480-124">The button is being clicked.</span></span><br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <span data-ttu-id="57480-125"><dt>**\_encapsulamento de TBSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="57480-125"><dt>**TBSTATE\_WRAP**</dt></span></span> </dl>                            | <span data-ttu-id="57480-126">O botão é seguido por uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="57480-126">The button is followed by a line break.</span></span> <span data-ttu-id="57480-127">O botão também deve ter o \_ estado habilitado TBSTATE.</span><span class="sxs-lookup"><span data-stu-id="57480-127">The button must also have the TBSTATE\_ENABLED state.</span></span><br/>                                              |



## <a name="remarks"></a><span data-ttu-id="57480-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="57480-128">Remarks</span></span>

<span data-ttu-id="57480-129">Uma barra de ferramentas pode ter uma combinação de Estados.</span><span class="sxs-lookup"><span data-stu-id="57480-129">A toolbar may have a combination of states.</span></span>

## <a name="requirements"></a><span data-ttu-id="57480-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57480-130">Requirements</span></span>



| <span data-ttu-id="57480-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="57480-131">Requirement</span></span> | <span data-ttu-id="57480-132">Valor</span><span class="sxs-lookup"><span data-stu-id="57480-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57480-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57480-133">Header</span></span><br/> | <dl> <span data-ttu-id="57480-134"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57480-134"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





