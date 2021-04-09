---
title: Mensagem de LB_FINDSTRINGEXACT (WinUser. h)
description: Localiza a primeira cadeia de caracteres da caixa de listagem que corresponde exatamente à cadeia de caracteres especificada, exceto que a pesquisa não diferencia maiúsculas de minúsculas.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- Controles de LB_FINDSTRINGEXACT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009716"
---
# <a name="lb_findstringexact-message"></a><span data-ttu-id="03786-104">FINDSTRINGEXACT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="03786-104">LB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="03786-105">Localiza a primeira cadeia de caracteres da caixa de listagem que corresponde exatamente à cadeia de caracteres especificada, exceto que a pesquisa não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="03786-105">Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive.</span></span>

## <a name="parameters"></a><span data-ttu-id="03786-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03786-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03786-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03786-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03786-108">O índice baseado em zero do item antes do primeiro item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="03786-108">The zero-based index of the item before the first item to be searched.</span></span> <span data-ttu-id="03786-109">Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará pesquisando da parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="03786-109">When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="03786-110">Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.</span><span class="sxs-lookup"><span data-stu-id="03786-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

<span data-ttu-id="03786-111">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="03786-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="03786-112">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="03786-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="03786-113">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="03786-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="03786-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03786-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03786-115">Um ponteiro para a cadeia de caracteres terminada em nulo para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="03786-115">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="03786-116">A pesquisa não diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="03786-116">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03786-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03786-117">Return value</span></span>

<span data-ttu-id="03786-118">O valor de retorno será o índice de base zero do item de correspondência ou o \_ erro de lb se a pesquisa não tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="03786-118">The return value is the zero-based index of the matching item, or LB\_ERR if the search was unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="03786-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="03786-119">Remarks</span></span>

<span data-ttu-id="03786-120">Essa função só será bem-sucedida se a cadeia de caracteres especificada e um item de caixa de listagem tiverem o mesmo comprimento (exceto para NULL no final da cadeia de caracteres especificada) e tiverem exatamente os mesmos caracteres.</span><span class="sxs-lookup"><span data-stu-id="03786-120">This function is only successful if the specified string and a list box item have the same length (except for the null at the end of the specified string) and have exactly the same characters.</span></span>

<span data-ttu-id="03786-121">Se a caixa de listagem tiver o estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , a ação executada por **lb \_ FINDSTRINGEXACT** dependerá de o estilo de [**\_ classificação lbs**](list-box-styles.md) ser usado.</span><span class="sxs-lookup"><span data-stu-id="03786-121">If the list box has the owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the action taken by **LB\_FINDSTRINGEXACT** depends on whether the [**LBS\_SORT**](list-box-styles.md) style is used.</span></span> <span data-ttu-id="03786-122">Se **a \_ classificação de lbs** for usada, o sistema enviará mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) para o proprietário da caixa de listagem para determinar qual item corresponde à cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="03786-122">If **LBS\_SORT** is used, the system sends [**WM\_COMPAREITEM**](wm-compareitem.md) messages to the list box owner to determine which item matches the specified string.</span></span> <span data-ttu-id="03786-123">Caso contrário, o **lb \_ FINDSTRINGEXACT** tentará localizar um item que tenha um valor longo (fornecido como o parâmetro *lParam* da mensagem de [**\_ inserção**](lb-insertstring.md) [**\_ AddString**](lb-addstring.md) ou lb) do lb que corresponda ao parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="03786-123">Otherwise, **LB\_FINDSTRINGEXACT** attempts to find an item that has a long value (supplied as the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message) that matches the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="03786-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03786-124">Requirements</span></span>



| <span data-ttu-id="03786-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="03786-125">Requirement</span></span> | <span data-ttu-id="03786-126">Valor</span><span class="sxs-lookup"><span data-stu-id="03786-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03786-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03786-127">Minimum supported client</span></span><br/> | <span data-ttu-id="03786-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03786-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03786-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03786-129">Minimum supported server</span></span><br/> | <span data-ttu-id="03786-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03786-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03786-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03786-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="03786-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03786-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03786-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="03786-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03786-134">**Localizar LBstring \_**</span><span class="sxs-lookup"><span data-stu-id="03786-134">**LB\_FINDSTRING**</span></span>](lb-findstring.md)
</dt> </dl>

 

 





