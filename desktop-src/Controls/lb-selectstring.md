---
title: Mensagem de LB_SELECTSTRING (WinUser. h)
description: Pesquisa uma caixa de listagem para um item que começa com os caracteres em uma cadeia de caracteres especificada. Se um item correspondente for encontrado, o item será selecionado.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- Controles de LB_SELECTSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5963ea6530038e17bc7f23d9ab66eba14ca0b05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455757"
---
# <a name="lb_selectstring-message"></a><span data-ttu-id="5319d-105">\_Mensagem SelectString do lb</span><span class="sxs-lookup"><span data-stu-id="5319d-105">LB\_SELECTSTRING message</span></span>

<span data-ttu-id="5319d-106">Pesquisa uma caixa de listagem para um item que começa com os caracteres em uma cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="5319d-106">Searches a list box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="5319d-107">Se um item correspondente for encontrado, o item será selecionado.</span><span class="sxs-lookup"><span data-stu-id="5319d-107">If a matching item is found, the item is selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="5319d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5319d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5319d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5319d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5319d-110">O índice baseado em zero do item antes do primeiro item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="5319d-110">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="5319d-111">Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará na parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="5319d-111">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="5319d-112">Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.</span><span class="sxs-lookup"><span data-stu-id="5319d-112">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="5319d-113">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5319d-113">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="5319d-114">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="5319d-114">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="5319d-115">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="5319d-115">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="5319d-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5319d-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5319d-117">Um ponteiro para a cadeia de caracteres terminada em nulo que contém o prefixo a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="5319d-117">A pointer to the null-terminated string that contains the prefix for which to search.</span></span> <span data-ttu-id="5319d-118">A pesquisa diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5319d-118">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5319d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5319d-119">Return value</span></span>

<span data-ttu-id="5319d-120">Se a pesquisa for bem-sucedida, o valor de retorno será o índice do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="5319d-120">If the search is successful, the return value is the index of the selected item.</span></span> <span data-ttu-id="5319d-121">Se a pesquisa não for bem-sucedida, o valor de retorno será de \_ erro lb e a seleção atual não será alterada.</span><span class="sxs-lookup"><span data-stu-id="5319d-121">If the search is unsuccessful, the return value is LB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5319d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5319d-122">Remarks</span></span>

<span data-ttu-id="5319d-123">A caixa de listagem é rolada, se necessário, para colocar o item selecionado em exibição.</span><span class="sxs-lookup"><span data-stu-id="5319d-123">The list box is scrolled, if necessary, to bring the selected item into view.</span></span>

<span data-ttu-id="5319d-124">Não use essa mensagem com uma caixa de listagem que tenha os estilos de [**lbs \_ MULTIPLESEL**](list-box-styles.md) ou [**lbs \_ EXTENDEDSEL**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5319d-124">Do not use this message with a list box that has the [**LBS\_MULTIPLESEL**](list-box-styles.md) or the [**LBS\_EXTENDEDSEL**](list-box-styles.md) styles.</span></span>

<span data-ttu-id="5319d-125">Um item será selecionado somente se seus caracteres iniciais do ponto de partida corresponderem aos caracteres na cadeia de caracteres especificada pelo parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5319d-125">An item is selected only if its initial characters from the starting point match the characters in the string specified by the *lParam* parameter.</span></span>

<span data-ttu-id="5319d-126">Se a caixa de listagem tiver o estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , a ação tomada por **lb \_ SelectString** dependerá de o estilo de [**\_ classificação lbs**](list-box-styles.md) ser usado.</span><span class="sxs-lookup"><span data-stu-id="5319d-126">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_SELECTSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="5319d-127">Se **a \_ classificação de lbs** for usada, o sistema enviará mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) para o proprietário da caixa de listagem para determinar qual item corresponde à cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="5319d-127">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="5319d-128">Caso contrário, o **lb \_ SelectString** tentará localizar um item que tem um valor longo (fornecido como o parâmetro *lParam* da mensagem do [**lb \_ AddString**](lb-addstring.md) ou [**lbstring \_**](lb-insertstring.md) ) que corresponde ao parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5319d-128">Otherwise, **LB\_SELECTSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5319d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5319d-129">Requirements</span></span>



| <span data-ttu-id="5319d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5319d-130">Requirement</span></span> | <span data-ttu-id="5319d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5319d-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5319d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5319d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5319d-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5319d-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5319d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5319d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5319d-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5319d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5319d-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5319d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5319d-137"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5319d-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5319d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5319d-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="5319d-139">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5319d-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5319d-140">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="5319d-140">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="5319d-141">**Localizar LBstring \_**</span><span class="sxs-lookup"><span data-stu-id="5319d-141">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> <dt>

[<span data-ttu-id="5319d-142">**KG \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="5319d-142">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





