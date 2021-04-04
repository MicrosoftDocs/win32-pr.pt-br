---
title: Mensagem de CB_GETLBTEXTLEN (WinUser. h)
description: Obtém o comprimento, em caracteres, de uma cadeia de caracteres na lista de uma caixa de combinação.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- Controles de CB_GETLBTEXTLEN de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918434"
---
# <a name="cb_getlbtextlen-message"></a><span data-ttu-id="975b0-104">\_Mensagem de GETLBTEXTLEN CB</span><span class="sxs-lookup"><span data-stu-id="975b0-104">CB\_GETLBTEXTLEN message</span></span>

<span data-ttu-id="975b0-105">Obtém o comprimento, em caracteres, de uma cadeia de caracteres na lista de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="975b0-105">Gets the length, in characters, of a string in the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="975b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="975b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="975b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="975b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="975b0-108">O índice de base zero da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="975b0-108">The zero-based index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="975b0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="975b0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="975b0-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="975b0-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="975b0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="975b0-111">Return value</span></span>

<span data-ttu-id="975b0-112">O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="975b0-112">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="975b0-113">Se uma cadeia de caracteres ANSI for o número de bytes e se for uma cadeia de caracteres Unicode, esse será o número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="975b0-113">If an ANSI string this is the number of bytes, and if it is a Unicode string this is the number of characters.</span></span> <span data-ttu-id="975b0-114">Em determinadas condições, esse valor pode ser, na verdade, maior que o comprimento do texto.</span><span class="sxs-lookup"><span data-stu-id="975b0-114">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="975b0-115">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="975b0-115">For more information, see the Remarks section.</span></span>

<span data-ttu-id="975b0-116">Se o parâmetro *wParam* não especificar um índice válido, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="975b0-116">If the *wParam* parameter does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="975b0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="975b0-117">Remarks</span></span>

<span data-ttu-id="975b0-118">Em determinadas condições, o valor de retorno é maior do que o comprimento real do texto.</span><span class="sxs-lookup"><span data-stu-id="975b0-118">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="975b0-119">Isso ocorre com determinadas misturas de ANSI e Unicode e é devido ao sistema operacional permitir a possível existência de caracteres de conjunto de caracteres de dois bytes (DBCS) dentro do texto.</span><span class="sxs-lookup"><span data-stu-id="975b0-119">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="975b0-120">O valor de retorno, no entanto, sempre será pelo menos tão grande quanto o comprimento real do texto; Portanto, você sempre pode usá-lo para guiar a alocação do buffer.</span><span class="sxs-lookup"><span data-stu-id="975b0-120">The return value, however, will always be at least as large as the actual length of the text; so you can always use it to guide buffer allocation.</span></span> <span data-ttu-id="975b0-121">Esse comportamento pode ocorrer quando um aplicativo usa funções ANSI e caixas de diálogo comuns, que usam Unicode.</span><span class="sxs-lookup"><span data-stu-id="975b0-121">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="975b0-122">Para obter o comprimento exato do texto, use as mensagens [**do \_ WM gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)ou [**CB \_ GETLBTEXT**](cb-getlbtext.md) ou a função [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="975b0-122">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="975b0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="975b0-123">Requirements</span></span>



| <span data-ttu-id="975b0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="975b0-124">Requirement</span></span> | <span data-ttu-id="975b0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="975b0-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="975b0-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="975b0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="975b0-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="975b0-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="975b0-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="975b0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="975b0-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="975b0-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="975b0-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="975b0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="975b0-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="975b0-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="975b0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="975b0-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="975b0-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="975b0-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="975b0-134">**\_GETLBTEXT CB**</span><span class="sxs-lookup"><span data-stu-id="975b0-134">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="975b0-135">**LB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="975b0-135">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="975b0-136">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="975b0-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="975b0-137">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="975b0-137">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="975b0-138">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="975b0-138">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

