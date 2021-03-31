---
title: Mensagem de EM_PASTESPECIAL (RichEdit. h)
description: Cola um formato de área de transferência específico em um controle de edição rico.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- Controles de EM_PASTESPECIAL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824530"
---
# <a name="em_pastespecial-message"></a><span data-ttu-id="1dfbb-104">\_Mensagem em PASTESPECIAL</span><span class="sxs-lookup"><span data-stu-id="1dfbb-104">EM\_PASTESPECIAL message</span></span>

<span data-ttu-id="1dfbb-105">Cola um formato de área de transferência específico em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-105">Pastes a specific clipboard format in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1dfbb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dfbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfbb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1dfbb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfbb-108">Especifica os [formatos da área de transferência](/windows/desktop/dataxchg/clipboard-formats).</span><span class="sxs-lookup"><span data-stu-id="1dfbb-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats).</span></span>

</dd> <dt>

<span data-ttu-id="1dfbb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1dfbb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfbb-110">Ponteiro para uma estrutura [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-110">Pointer to a [**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) structure or **NULL**.</span></span> <span data-ttu-id="1dfbb-111">Se um objeto estiver sendo colado, a estrutura **REPASTESPECIAL** será preenchida com o aspecto de exibição desejado.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-111">If an object is being pasted, the **REPASTESPECIAL** structure is filled in with the desired display aspect.</span></span> <span data-ttu-id="1dfbb-112">Se *lParam* for **nulo** ou o membro **dwAspect** for zero, o aspecto de exibição usado será o conteúdo do descritor de objeto.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-112">If *lParam* is **NULL** or the **dwAspect** member is zero, the display aspect used will be the contents of the object descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfbb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1dfbb-113">Return value</span></span>

<span data-ttu-id="1dfbb-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1dfbb-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfbb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dfbb-115">Requirements</span></span>



| <span data-ttu-id="1dfbb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dfbb-116">Requirement</span></span> | <span data-ttu-id="1dfbb-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1dfbb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfbb-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dfbb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfbb-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1dfbb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1dfbb-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dfbb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfbb-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1dfbb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dfbb-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1dfbb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfbb-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dfbb-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfbb-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dfbb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfbb-125">**REPASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="1dfbb-125">**REPASTESPECIAL**</span></span>](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

