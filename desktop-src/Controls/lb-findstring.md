---
title: Mensagem de LB_FINDSTRING (WinUser. h)
description: Localiza a primeira cadeia de caracteres em uma caixa de listagem que começa com a cadeia de caracteres especificada.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- Controles de LB_FINDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455896"
---
# <a name="lb_findstring-message"></a><span data-ttu-id="e1230-104">\_Mensagem de localização lb</span><span class="sxs-lookup"><span data-stu-id="e1230-104">LB\_FINDSTRING message</span></span>

<span data-ttu-id="e1230-105">Localiza a primeira cadeia de caracteres em uma caixa de listagem que começa com a cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="e1230-105">Finds the first string in a list box that begins with the specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1230-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1230-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1230-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e1230-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1230-108">O índice baseado em zero do item antes do primeiro item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="e1230-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="e1230-109">Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará pesquisando da parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e1230-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="e1230-110">Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.</span><span class="sxs-lookup"><span data-stu-id="e1230-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="e1230-111">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e1230-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="e1230-112">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="e1230-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="e1230-113">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="e1230-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="e1230-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e1230-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e1230-115">Um ponteiro para a cadeia de caracteres terminada em nulo que contém a cadeia de caracteres a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="e1230-115">A pointer to the null-terminated string that contains the string for which to search.</span></span> <span data-ttu-id="e1230-116">A pesquisa diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e1230-116">The search is case independent, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1230-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1230-117">Return value</span></span>

<span data-ttu-id="e1230-118">O valor de retorno será o índice do item correspondente ou o \_ erro de lb se a pesquisa não tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e1230-118">The return value is the index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1230-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1230-119">Remarks</span></span>

<span data-ttu-id="e1230-120">Se a caixa de listagem tiver o estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , a ação executada pela **\_ localização do lb** dependerá se o estilo de [**\_ classificação lbs**](list-box-styles.md) for usado.</span><span class="sxs-lookup"><span data-stu-id="e1230-120">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRING** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="e1230-121">Se **a \_ classificação de lbs** for usada, o sistema enviará mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) para o proprietário da caixa de listagem para determinar qual item corresponde à cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="e1230-121">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="e1230-122">Caso contrário, o **lb \_ FindString** tentará localizar um item que tem um valor longo (fornecido como o parâmetro *lParam* da mensagem do [**lb \_ AddString**](lb-addstring.md) ou [**lbstring \_**](lb-insertstring.md) ) que corresponde ao parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e1230-122">Otherwise, **LB\_FINDSTRING** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1230-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1230-123">Requirements</span></span>



| <span data-ttu-id="e1230-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1230-124">Requirement</span></span> | <span data-ttu-id="e1230-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e1230-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1230-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1230-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e1230-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e1230-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e1230-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1230-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e1230-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e1230-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e1230-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1230-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1230-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1230-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1230-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1230-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1230-133">**\_FINDSTRINGEXACT lb**</span><span class="sxs-lookup"><span data-stu-id="e1230-133">**LB\_FINDSTRINGEXACT**</span></span>](lb-findstringexact.md)
</dt> </dl>

 

 





