---
title: Mensagem de LB_GETTEXTLEN (WinUser. h)
description: Obtém o comprimento de uma cadeia de caracteres em uma caixa de listagem.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- Controles de LB_GETTEXTLEN de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085465"
---
# <a name="lb_gettextlen-message"></a><span data-ttu-id="6ca26-104">GETTEXTLEN de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="6ca26-104">LB\_GETTEXTLEN message</span></span>

<span data-ttu-id="6ca26-105">Obtém o comprimento de uma cadeia de caracteres em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="6ca26-105">Gets the length of a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ca26-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ca26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca26-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ca26-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ca26-108">O índice de base zero da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6ca26-108">The zero-based index of the string.</span></span>

<span data-ttu-id="6ca26-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6ca26-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="6ca26-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="6ca26-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="6ca26-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="6ca26-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="6ca26-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ca26-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ca26-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6ca26-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ca26-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ca26-114">Return value</span></span>

<span data-ttu-id="6ca26-115">O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="6ca26-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="6ca26-116">Em determinadas condições, esse valor pode ser, na verdade, maior que o comprimento do texto.</span><span class="sxs-lookup"><span data-stu-id="6ca26-116">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="6ca26-117">Para obter mais informações, consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ca26-117">For more information, see the following Remarks section.</span></span>

<span data-ttu-id="6ca26-118">Se o parâmetro *wParam* não especificar um índice válido, o valor de retorno será um \_ erro de lb.</span><span class="sxs-lookup"><span data-stu-id="6ca26-118">If the *wParam* parameter does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca26-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ca26-119">Remarks</span></span>

<span data-ttu-id="6ca26-120">Em determinadas condições, o valor de retorno é maior do que o comprimento real do texto.</span><span class="sxs-lookup"><span data-stu-id="6ca26-120">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="6ca26-121">Isso ocorre com determinadas misturas de ANSI e Unicode e é devido ao sistema operacional permitir a possível existência de caracteres de conjunto de caracteres de dois bytes (DBCS) dentro do texto.</span><span class="sxs-lookup"><span data-stu-id="6ca26-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="6ca26-122">O valor de retorno, no entanto, sempre será pelo menos tão grande quanto o comprimento real do texto; Portanto, você pode usá-lo sempre para orientar a alocação do buffer.</span><span class="sxs-lookup"><span data-stu-id="6ca26-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="6ca26-123">Esse comportamento pode ocorrer quando um aplicativo usa funções ANSI e caixas de diálogo comuns, que usam Unicode.</span><span class="sxs-lookup"><span data-stu-id="6ca26-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="6ca26-124">Para obter o comprimento exato do texto, use as mensagens [**do \_ WM gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)ou [**CB \_ GETLBTEXT**](cb-getlbtext.md) ou a função [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="6ca26-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="6ca26-125">Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , o valor de retorno será sempre o tamanho, em bytes, de um **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="6ca26-125">If the list box has an owner-drawn style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the return value is always the size, in bytes, of a **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca26-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ca26-126">Requirements</span></span>



| <span data-ttu-id="6ca26-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ca26-127">Requirement</span></span> | <span data-ttu-id="6ca26-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6ca26-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca26-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca26-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca26-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ca26-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6ca26-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca26-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca26-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ca26-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6ca26-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ca26-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca26-134"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ca26-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca26-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ca26-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ca26-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6ca26-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6ca26-137">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="6ca26-137">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="6ca26-138">**LB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="6ca26-138">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="6ca26-139">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="6ca26-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6ca26-140">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="6ca26-140">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="6ca26-141">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="6ca26-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

