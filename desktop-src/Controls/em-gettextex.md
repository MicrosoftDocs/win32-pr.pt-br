---
title: Mensagem de EM_GETTEXTEX (RichEdit. h)
description: Obtém o texto de um controle de edição rico.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- Controles de EM_GETTEXTEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455067"
---
# <a name="em_gettextex-message"></a><span data-ttu-id="77f28-104">\_Mensagem em GETTEXTEX</span><span class="sxs-lookup"><span data-stu-id="77f28-104">EM\_GETTEXTEX message</span></span>

<span data-ttu-id="77f28-105">Obtém o texto de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="77f28-105">Gets the text from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="77f28-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77f28-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77f28-108">Ponteiro para uma estrutura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , que indica como converter o texto antes de colocá-lo no buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="77f28-108">Pointer to a [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure, which indicates how to translate the text before putting it into the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="77f28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77f28-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77f28-110">Ponteiro para o buffer para receber o texto.</span><span class="sxs-lookup"><span data-stu-id="77f28-110">Pointer to the buffer to receive the text.</span></span> <span data-ttu-id="77f28-111">O tamanho desse buffer, em bytes, é especificado pelo membro **CB** da estrutura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) .</span><span class="sxs-lookup"><span data-stu-id="77f28-111">The size of this buffer, in bytes, is specified by the **cb** member of the [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure.</span></span> <span data-ttu-id="77f28-112">Use a mensagem em [**\_ GETTEXTLENGTHEX**](em-gettextlengthex.md) para obter o tamanho necessário do buffer.</span><span class="sxs-lookup"><span data-stu-id="77f28-112">Use the [**EM\_GETTEXTLENGTHEX**](em-gettextlengthex.md) message to get the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77f28-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77f28-113">Return value</span></span>

<span data-ttu-id="77f28-114">O valor de retorno é o número de **TCHAR** s copiadas no buffer de saída, incluindo o terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="77f28-114">The return value is the number of **TCHAR** s copied into the output buffer, including the null terminator.</span></span>

## <a name="remarks"></a><span data-ttu-id="77f28-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="77f28-115">Remarks</span></span>

<span data-ttu-id="77f28-116">Se o tamanho do buffer de saída for menor que o tamanho do texto no controle, o controle de edição copiará o texto do seu início e o posicionará no buffer até que o buffer esteja cheio.</span><span class="sxs-lookup"><span data-stu-id="77f28-116">If the size of the output buffer is less than the size of the text in the control, the edit control will copy text from its beginning and place it in the buffer until the buffer is full.</span></span> <span data-ttu-id="77f28-117">Um caractere nulo de terminação ainda será colocado no final do buffer.</span><span class="sxs-lookup"><span data-stu-id="77f28-117">A terminating null character will still be placed at the end of the buffer.</span></span>

<span data-ttu-id="77f28-118">Se o texto ANSI for solicitado, em **\_ GETTEXTEX** usará a função [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para converter os caracteres Unicode em ANSI.</span><span class="sxs-lookup"><span data-stu-id="77f28-118">If ANSI text is requested, **EM\_GETTEXTEX** uses the [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function to translate the Unicode characters to ANSI.</span></span> <span data-ttu-id="77f28-119">Ele permite que você vá de Unicode para ANSI usando uma página de código específica.</span><span class="sxs-lookup"><span data-stu-id="77f28-119">It allows you to go from Unicode to ANSI using a particular code page.</span></span> <span data-ttu-id="77f28-120">A estrutura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contém membros (**lpDefaultChar** e **lpUsedDefChar**) que são usados na conversão de Unicode para ANSI.</span><span class="sxs-lookup"><span data-stu-id="77f28-120">The [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure contains members (**lpDefaultChar** and **lpUsedDefChar**) that are used in the translation from Unicode to ANSI.</span></span>

## <a name="requirements"></a><span data-ttu-id="77f28-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77f28-121">Requirements</span></span>



| <span data-ttu-id="77f28-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f28-122">Requirement</span></span> | <span data-ttu-id="77f28-123">Valor</span><span class="sxs-lookup"><span data-stu-id="77f28-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77f28-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77f28-124">Minimum supported client</span></span><br/> | <span data-ttu-id="77f28-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77f28-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77f28-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77f28-126">Minimum supported server</span></span><br/> | <span data-ttu-id="77f28-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77f28-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77f28-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77f28-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="77f28-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="77f28-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f28-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="77f28-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="77f28-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="77f28-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="77f28-132">**em \_ SETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="77f28-132">**EM\_SETTEXTEX**</span></span>](em-settextex.md)
</dt> <dt>

[<span data-ttu-id="77f28-133">**GETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="77f28-133">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

<span data-ttu-id="77f28-134">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="77f28-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="77f28-135">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="77f28-135">**WideCharToMultiByte**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[<span data-ttu-id="77f28-136">**SetText do WM \_**</span><span class="sxs-lookup"><span data-stu-id="77f28-136">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

