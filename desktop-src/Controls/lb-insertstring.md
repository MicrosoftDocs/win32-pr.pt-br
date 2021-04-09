---
title: Mensagem de LB_INSERTSTRING (WinUser. h)
description: Insere uma cadeia de caracteres ou dados de item em uma caixa de listagem. Ao contrário da \_ mensagem de AddString do lb, a mensagem de inserção de lb não faz com \_ que uma lista com o \_ estilo de classificação lbs seja classificada.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- Controles de LB_INSERTSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086177"
---
# <a name="lb_insertstring-message"></a><span data-ttu-id="b1d7f-105">Mensagem de inserção de LB \_</span><span class="sxs-lookup"><span data-stu-id="b1d7f-105">LB\_INSERTSTRING message</span></span>

<span data-ttu-id="b1d7f-106">Insere uma cadeia de caracteres ou dados de item em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-106">Inserts a string or item data into a list box.</span></span> <span data-ttu-id="b1d7f-107">Ao contrário da mensagem de [**\_ AddString do lb**](lb-addstring.md) , a mensagem de **\_ inserção de lb** não faz com que uma lista com o estilo de [**\_ classificação lbs**](list-box-styles.md) seja classificada.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-107">Unlike the [**LB\_ADDSTRING**](lb-addstring.md) message, the **LB\_INSERTSTRING** message does not cause a list with the [**LBS\_SORT**](list-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1d7f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1d7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1d7f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1d7f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1d7f-110">O índice de base zero da posição na qual inserir a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="b1d7f-111">Se esse parâmetro for-1, a cadeia de caracteres será adicionada ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="b1d7f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1d7f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1d7f-113">Um ponteiro para a cadeia de caracteres terminada em nulo a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="b1d7f-114">Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , esse parâmetro será armazenado como dados de item em vez de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this parameter is stored as item data instead of a string.</span></span> <span data-ttu-id="b1d7f-115">Você pode enviar as [**mensagens \_ GETITEMDATA**](lb-getitemdata.md) e [**lb \_ SETITEMDATA**](lb-setitemdata.md) para recuperar ou modificar os dados do item.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-115">You can send the [**LB\_GETITEMDATA**](lb-getitemdata.md) and [**LB\_SETITEMDATA**](lb-setitemdata.md) messages to retrieve or modify the item data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1d7f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1d7f-116">Return value</span></span>

<span data-ttu-id="b1d7f-117">O valor de retorno é o índice da posição na qual a cadeia de caracteres foi inserida.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-117">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="b1d7f-118">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="b1d7f-118">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="b1d7f-119">Se não houver espaço suficiente para armazenar a nova cadeia de caracteres, o valor de retorno será LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-119">If there is insufficient space to store the new string, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1d7f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1d7f-120">Remarks</span></span>

<span data-ttu-id="b1d7f-121">A [**mensagem \_ INITSTORAGE de lb**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100).</span><span class="sxs-lookup"><span data-stu-id="b1d7f-121">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="b1d7f-122">Ele reserva a quantidade especificada de memória para que as mensagens de **\_ inserção de lb** subsequentes tenham o menor tempo possível.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-122">It reserves the specified amount of memory so that subsequent **LB\_INSERTSTRING** messages take the shortest possible time.</span></span> <span data-ttu-id="b1d7f-123">Você pode usar estimativas para os parâmetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b1d7f-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="b1d7f-124">Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="b1d7f-125">Se a caixa de listagem tiver o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e você inserir uma cadeia de caracteres maior que a caixa de listagem, envie uma mensagem [**\_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-125">If the list box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the list box, send an [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="b1d7f-126">Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-126">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="b1d7f-127">Isso pode causar problemas.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-127">This can cause problems.</span></span> <span data-ttu-id="b1d7f-128">Por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode no Windows em Japonês ficarão confusos.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-128">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="b1d7f-129">Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="b1d7f-129">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d7f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1d7f-130">Requirements</span></span>



| <span data-ttu-id="b1d7f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1d7f-131">Requirement</span></span> | <span data-ttu-id="b1d7f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b1d7f-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d7f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1d7f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d7f-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1d7f-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b1d7f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1d7f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d7f-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1d7f-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1d7f-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1d7f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1d7f-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1d7f-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1d7f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1d7f-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1d7f-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b1d7f-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1d7f-141">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="b1d7f-141">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="b1d7f-142">**seleção de LBstring \_**</span><span class="sxs-lookup"><span data-stu-id="b1d7f-142">**LB\_SELECTSTRING**</span></span>](lb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="b1d7f-143">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="b1d7f-143">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> </dl>

 

