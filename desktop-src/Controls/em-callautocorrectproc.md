---
title: Mensagem de EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Chama a função de retorno de chamada de AutoCorreção armazenada pela \_ mensagem em SETAUTOCORRECTPROC, desde que o texto anterior ao ponto de inserção seja um candidato para correção automática.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- Controles de EM_CALLAUTOCORRECTPROC de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455449"
---
# <a name="em_callautocorrectproc-message"></a><span data-ttu-id="5f396-104">\_Mensagem em CALLAUTOCORRECTPROC</span><span class="sxs-lookup"><span data-stu-id="5f396-104">EM\_CALLAUTOCORRECTPROC message</span></span>

<span data-ttu-id="5f396-105">Chama a função de retorno de chamada de AutoCorreção armazenada pela mensagem em [**\_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md) , desde que o texto anterior ao ponto de inserção seja um candidato para correção automática.</span><span class="sxs-lookup"><span data-stu-id="5f396-105">Calls the autocorrect callback function that is stored by the [**EM\_SETAUTOCORRECTPROC**](em-setautocorrectproc.md) message, provided that the text preceding the insertion point is a candidate for autocorrection.</span></span>


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a><span data-ttu-id="5f396-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f396-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f396-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f396-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f396-108">Um caractere do tipo **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="5f396-108">A character of type **WCHAR**.</span></span> <span data-ttu-id="5f396-109">Se esse caractere for uma tabulação (U + 0009) e o caractere que precede o ponto de inserção não for uma guia, o caractere que precede o ponto de inserção será tratado como parte da cadeia de caracteres de candidato à AutoCorreção em vez de como um delimitador de cadeia de caracteres; caso contrário, *wParam* não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="5f396-109">If this character is a tab (U+0009), and the character preceding the insertion point isn t a tab, then the character preceding the insertion point is treated as part of the autocorrect candidate string instead of as a string delimiter; otherwise, *wParam* has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="5f396-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f396-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f396-111">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5f396-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f396-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f396-112">Return value</span></span>

<span data-ttu-id="5f396-113">O valor de retorno será zero se a mensagem tiver sucesso ou for diferente de zero se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="5f396-113">The return value is zero if the message succeeds, or nonzero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f396-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f396-114">Requirements</span></span>



| <span data-ttu-id="5f396-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f396-115">Requirement</span></span> | <span data-ttu-id="5f396-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5f396-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f396-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f396-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5f396-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5f396-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5f396-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f396-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5f396-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5f396-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f396-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f396-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f396-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f396-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f396-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f396-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f396-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="5f396-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="5f396-125">**em \_ GETAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="5f396-125">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="5f396-126">**em \_ SETAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="5f396-126">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





