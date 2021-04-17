---
title: Mensagem de LB_SETCURSEL (WinUser. h)
description: Seleciona uma cadeia de caracteres e a rola para a exibição, se necessário. Quando a nova cadeia de caracteres é selecionada, a caixa de listagem remove o realce da cadeia de caracteres selecionada anteriormente.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- Controles de LB_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d1305ccece9c220d6a20e72e0ee54a428f8b13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751151"
---
# <a name="lb_setcursel-message"></a><span data-ttu-id="bedb7-105">\_Mensagem de DEcursão de lb</span><span class="sxs-lookup"><span data-stu-id="bedb7-105">LB\_SETCURSEL message</span></span>

<span data-ttu-id="bedb7-106">Seleciona uma cadeia de caracteres e a rola para a exibição, se necessário.</span><span class="sxs-lookup"><span data-stu-id="bedb7-106">Selects a string and scrolls it into view, if necessary.</span></span> <span data-ttu-id="bedb7-107">Quando a nova cadeia de caracteres é selecionada, a caixa de listagem remove o realce da cadeia de caracteres selecionada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="bedb7-107">When the new string is selected, the list box removes the highlight from the previously selected string.</span></span>

## <a name="parameters"></a><span data-ttu-id="bedb7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bedb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bedb7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bedb7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bedb7-110">Especifica o índice de base zero da cadeia de caracteres selecionada.</span><span class="sxs-lookup"><span data-stu-id="bedb7-110">Specifies the zero-based index of the string that is selected.</span></span> <span data-ttu-id="bedb7-111">Se esse parâmetro for-1, a caixa de listagem será definida como sem seleção.</span><span class="sxs-lookup"><span data-stu-id="bedb7-111">If this parameter is -1, the list box is set to have no selection.</span></span>

<span data-ttu-id="bedb7-112">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="bedb7-112">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="bedb7-113">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="bedb7-113">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="bedb7-114">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="bedb7-114">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="bedb7-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bedb7-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bedb7-116">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="bedb7-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bedb7-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bedb7-117">Return value</span></span>

<span data-ttu-id="bedb7-118">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="bedb7-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="bedb7-119">Se o parâmetro *wParam* for-1, o valor de retorno será de \_ erro lb mesmo que nenhum erro tenha ocorrido.</span><span class="sxs-lookup"><span data-stu-id="bedb7-119">If the *wParam* parameter is -1, the return value is LB\_ERR even though no error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="bedb7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="bedb7-120">Remarks</span></span>

<span data-ttu-id="bedb7-121">Use essa mensagem somente com caixas de listagem de seleção única.</span><span class="sxs-lookup"><span data-stu-id="bedb7-121">Use this message only with single-selection list boxes.</span></span> <span data-ttu-id="bedb7-122">Você não pode usá-lo para definir ou remover uma seleção em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="bedb7-122">You cannot use it to set or remove a selection in a multiple-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="bedb7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bedb7-123">Requirements</span></span>



| <span data-ttu-id="bedb7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bedb7-124">Requirement</span></span> | <span data-ttu-id="bedb7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bedb7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bedb7-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bedb7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bedb7-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bedb7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bedb7-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bedb7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bedb7-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bedb7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bedb7-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bedb7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bedb7-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bedb7-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bedb7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bedb7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bedb7-133">**KG \_ de lb**</span><span class="sxs-lookup"><span data-stu-id="bedb7-133">**LB\_GETCURSEL**</span></span>](lb-getcursel.md)
</dt> </dl>

 

 





