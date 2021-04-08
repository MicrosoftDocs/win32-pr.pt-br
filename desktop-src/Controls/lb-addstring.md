---
title: Mensagem de LB_ADDSTRING (WinUser. h)
description: Adiciona uma cadeia de caracteres a uma caixa de listagem. Se a caixa de listagem não tiver o \_ estilo de classificação lbs, a cadeia de caracteres será adicionada ao final da lista. Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificada.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- Controles de LB_ADDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009301"
---
# <a name="lb_addstring-message"></a><span data-ttu-id="aeb01-106">\_Mensagem de ADDSTRING lb</span><span class="sxs-lookup"><span data-stu-id="aeb01-106">LB\_ADDSTRING message</span></span>

<span data-ttu-id="aeb01-107">Adiciona uma cadeia de caracteres a uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="aeb01-107">Adds a string to a list box.</span></span> <span data-ttu-id="aeb01-108">Se a caixa de listagem não tiver o estilo de [**\_ classificação lbs**](list-box-styles.md) , a cadeia de caracteres será adicionada ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="aeb01-108">If the list box does not have the [**LBS\_SORT**](list-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="aeb01-109">Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificada.</span><span class="sxs-lookup"><span data-stu-id="aeb01-109">Otherwise, the string is inserted into the list and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="aeb01-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aeb01-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb01-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aeb01-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb01-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="aeb01-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="aeb01-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aeb01-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aeb01-114">Um ponteiro para a cadeia de caracteres terminada em nulo que deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="aeb01-114">A pointer to the null-terminated string that is to be added.</span></span>

<span data-ttu-id="aeb01-115">Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , esse parâmetro será armazenado como dados de item em vez de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="aeb01-115">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="aeb01-116">Você pode enviar as **mensagens \_ GETITEMDATA** e **lb \_ SETITEMDATA** para recuperar ou modificar os dados do item.</span><span class="sxs-lookup"><span data-stu-id="aeb01-116">You can send the **LB\_GETITEMDATA** and **LB\_SETITEMDATA** messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb01-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aeb01-117">Return value</span></span>

<span data-ttu-id="aeb01-118">O valor de retorno é o índice de base zero da cadeia de caracteres na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="aeb01-118">The return value is the zero-based index of the string in the list box.</span></span> <span data-ttu-id="aeb01-119">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="aeb01-119">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="aeb01-120">Se não houver espaço suficiente para armazenar a nova cadeia de caracteres, o valor de retorno será LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="aeb01-120">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb01-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="aeb01-121">Remarks</span></span>

<span data-ttu-id="aeb01-122">Se a caixa de listagem tiver um estilo desenhado pelo proprietário e o estilo de [**\_ classificação lbs**](list-box-styles.md) , mas não o estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , o sistema enviará a mensagem [**\_ COMPAREITEM do WM**](wm-compareitem.md) uma ou mais vezes para o proprietário da caixa de listagem para posicionar o novo item corretamente na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="aeb01-122">If the list box has an owner-drawn style and the [**LBS\_SORT**](list-box-styles.md) style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends the [**WM\_COMPAREITEM**](wm-compareitem.md) message one or more times to the owner of the list box to place the new item properly in the list box.</span></span>

<span data-ttu-id="aeb01-123">A [**mensagem \_ INITSTORAGE de lb**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100).</span><span class="sxs-lookup"><span data-stu-id="aeb01-123">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="aeb01-124">Ele reserva a quantidade especificada de memória para que as mensagens de **\_ cadeia de caracteres do lb** subsequentes tenham o menor tempo possível.</span><span class="sxs-lookup"><span data-stu-id="aeb01-124">It reserves the specified amount of memory so that subsequent **LB\_ADDSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="aeb01-125">Você pode usar estimativas para os parâmetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="aeb01-125">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="aeb01-126">Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="aeb01-126">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="aeb01-127">Se a caixa de listagem tiver o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e você adicionar uma cadeia de caracteres maior que a caixa de listagem, envie uma mensagem [**\_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.</span><span class="sxs-lookup"><span data-stu-id="aeb01-127">If the list box has the [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="aeb01-128">Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="aeb01-128">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="aeb01-129">Isso pode causar problemas.</span><span class="sxs-lookup"><span data-stu-id="aeb01-129">This can cause problems.</span></span> <span data-ttu-id="aeb01-130">Por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode no Windows em Japonês ficarão confusos.</span><span class="sxs-lookup"><span data-stu-id="aeb01-130">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="aeb01-131">Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="aeb01-131">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb01-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeb01-132">Requirements</span></span>



| <span data-ttu-id="aeb01-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb01-133">Requirement</span></span> | <span data-ttu-id="aeb01-134">Valor</span><span class="sxs-lookup"><span data-stu-id="aeb01-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb01-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeb01-135">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb01-136">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aeb01-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aeb01-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aeb01-137">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb01-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aeb01-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aeb01-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aeb01-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeb01-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aeb01-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb01-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="aeb01-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="aeb01-142">**Referência**</span><span class="sxs-lookup"><span data-stu-id="aeb01-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aeb01-143">**LB \_ DeleteString**</span><span class="sxs-lookup"><span data-stu-id="aeb01-143">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="aeb01-144">**KG \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="aeb01-144">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="aeb01-145">**seleção de LBstring \_**</span><span class="sxs-lookup"><span data-stu-id="aeb01-145">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="aeb01-146">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="aeb01-146">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="aeb01-147">**COMPAREITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="aeb01-147">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

