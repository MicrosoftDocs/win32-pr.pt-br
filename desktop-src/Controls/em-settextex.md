---
title: Mensagem de EM_SETTEXTEX (RichEdit. h)
description: Combina a funcionalidade das mensagens do WM \_ SetText e em \_ REPLACESEL e adiciona a capacidade de definir texto usando uma página de código e usar Rich Text ou texto sem formatação.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- Controles de EM_SETTEXTEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455344"
---
# <a name="em_settextex-message"></a><span data-ttu-id="164c5-104">\_Mensagem em SETTEXTEX</span><span class="sxs-lookup"><span data-stu-id="164c5-104">EM\_SETTEXTEX message</span></span>

<span data-ttu-id="164c5-105">Combina a funcionalidade das mensagens do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) e em [**\_ REPLACESEL**](em-replacesel.md) e adiciona a capacidade de definir texto usando uma página de código e usar Rich Text ou texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="164c5-105">Combines the functionality of the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) and [**EM\_REPLACESEL**](em-replacesel.md) messages, and adds the ability to set text using a code page and to use either rich text or plain text.</span></span>

## <a name="parameters"></a><span data-ttu-id="164c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="164c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="164c5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="164c5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="164c5-108">Ponteiro para uma estrutura [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) que especifica sinalizadores e uma página de código opcional a ser usada na tradução para Unicode.</span><span class="sxs-lookup"><span data-stu-id="164c5-108">Pointer to a [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) structure that specifies flags and an optional code page to use in translating to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="164c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="164c5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="164c5-110">Ponteiro para o texto terminado em nulo a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="164c5-110">Pointer to the null-terminated text to insert.</span></span> <span data-ttu-id="164c5-111">Esse texto é uma cadeia de caracteres ANSI, a menos que a página de código seja 1200 (Unicode).</span><span class="sxs-lookup"><span data-stu-id="164c5-111">This text is an ANSI string, unless the code page is 1200 (Unicode).</span></span> <span data-ttu-id="164c5-112">Se *lParam* começar com uma sequência ASCII de RTF válida, por exemplo, "{ \\ RTF" ou "{urtf", o texto será lido usando o leitor de RTF.</span><span class="sxs-lookup"><span data-stu-id="164c5-112">If *lParam* starts with a valid RTF ASCII sequence for example, "{\\rtf" or "{urtf" the text is read in using the RTF reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="164c5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="164c5-113">Return value</span></span>

<span data-ttu-id="164c5-114">Se a operação estiver definindo todo o texto e for bem sucedido, o valor de retorno será 1.</span><span class="sxs-lookup"><span data-stu-id="164c5-114">If the operation is setting all of the text and succeeds, the return value is 1.</span></span>

<span data-ttu-id="164c5-115">Se a operação estiver definindo a seleção e tiver sucesso, o valor de retorno será o número de bytes ou caracteres copiados.</span><span class="sxs-lookup"><span data-stu-id="164c5-115">If the operation is setting the selection and succeeds, the return value is the number of bytes or characters copied.</span></span>

<span data-ttu-id="164c5-116">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="164c5-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="164c5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="164c5-117">Requirements</span></span>



| <span data-ttu-id="164c5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="164c5-118">Requirement</span></span> | <span data-ttu-id="164c5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="164c5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="164c5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="164c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="164c5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="164c5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="164c5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="164c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="164c5-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="164c5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="164c5-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="164c5-124">Redistributable</span></span><br/>          | <span data-ttu-id="164c5-125">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="164c5-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="164c5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="164c5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="164c5-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="164c5-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="164c5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="164c5-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="164c5-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="164c5-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="164c5-130">**em \_ GETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="164c5-130">**EM\_GETTEXTEX**</span></span>](em-gettextex.md)
</dt> <dt>

[<span data-ttu-id="164c5-131">**SETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="164c5-131">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

