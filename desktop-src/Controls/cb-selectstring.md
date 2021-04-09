---
title: Mensagem de CB_SELECTSTRING (WinUser. h)
description: Pesquisa a lista de uma caixa de combinação de um item que começa com os caracteres em uma cadeia de caracteres especificada. Se um item correspondente for encontrado, ele será selecionado e copiado para o controle de edição.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- Controles de CB_SELECTSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009353"
---
# <a name="cb_selectstring-message"></a><span data-ttu-id="fbaf5-105">\_Mensagem SelectString do CB</span><span class="sxs-lookup"><span data-stu-id="fbaf5-105">CB\_SELECTSTRING message</span></span>

<span data-ttu-id="fbaf5-106">Pesquisa a lista de uma caixa de combinação de um item que começa com os caracteres em uma cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-106">Searches the list of a combo box for an item that begins with the characters in a specified string.</span></span> <span data-ttu-id="fbaf5-107">Se um item correspondente for encontrado, ele será selecionado e copiado para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-107">If a matching item is found, it is selected and copied to the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbaf5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbaf5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbaf5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbaf5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbaf5-110">O índice de base zero do item que antecede o primeiro item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-110">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="fbaf5-111">Quando a pesquisa atingir a parte inferior da lista, ela continuará na parte superior da lista de volta para o item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="fbaf5-111">When the search reaches the bottom of the list, it continues from the top of the list back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="fbaf5-112">Se *wParam* for-1, a lista inteira será pesquisada desde o início.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-112">If *wParam* is -1, the entire list is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="fbaf5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbaf5-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbaf5-114">Um ponteiro para a cadeia de caracteres terminada em nulo que contém os caracteres para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-114">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="fbaf5-115">A pesquisa não diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-115">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbaf5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbaf5-116">Return value</span></span>

<span data-ttu-id="fbaf5-117">Se a cadeia de caracteres for encontrada, o valor de retorno será o índice do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-117">If the string is found, the return value is the index of the selected item.</span></span> <span data-ttu-id="fbaf5-118">Se a pesquisa não for bem-sucedida, o valor de retorno será CB \_ Err e a seleção atual não será alterada.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-118">If the search is unsuccessful, the return value is CB\_ERR and the current selection is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbaf5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbaf5-119">Remarks</span></span>

<span data-ttu-id="fbaf5-120">Uma cadeia de caracteres será selecionada somente se os caracteres do ponto inicial corresponderem aos caracteres na cadeia de caracteres do prefixo.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-120">A string is selected only if the characters from the starting point match the characters in the prefix string.</span></span>

<span data-ttu-id="fbaf5-121">Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o que a mensagem **\_ SelectString do CB** dependerá se você usar o estilo de [**\_ classificação CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fbaf5-121">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_SELECTSTRING** message does depends on whether you use the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="fbaf5-122">Se o estilo de **\_ classificação CBS** for usado, o sistema enviará mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) para o proprietário da caixa de combinação para determinar qual item corresponde à cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="fbaf5-122">If the **CBS\_SORT** style is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="fbaf5-123">Se você não usar o estilo **de \_ classificação CBS** , o **CB \_ SelectString** tentará corresponder o valor **DWORD** em relação ao valor do parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="fbaf5-123">If you do not use the **CBS\_SORT** style, **CB\_SELECTSTRING** attempts to match the **DWORD** value against the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbaf5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbaf5-124">Requirements</span></span>



| <span data-ttu-id="fbaf5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbaf5-125">Requirement</span></span> | <span data-ttu-id="fbaf5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fbaf5-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbaf5-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbaf5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fbaf5-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fbaf5-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fbaf5-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbaf5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fbaf5-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fbaf5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fbaf5-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbaf5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbaf5-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbaf5-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbaf5-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbaf5-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="fbaf5-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="fbaf5-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fbaf5-135">**localização da CB \_**</span><span class="sxs-lookup"><span data-stu-id="fbaf5-135">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="fbaf5-136">**\_FINDSTRINGEXACT CB**</span><span class="sxs-lookup"><span data-stu-id="fbaf5-136">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="fbaf5-137">**CB \_ SETcurseal**</span><span class="sxs-lookup"><span data-stu-id="fbaf5-137">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="fbaf5-138">**COMPAREITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="fbaf5-138">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





