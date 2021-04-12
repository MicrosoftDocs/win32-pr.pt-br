---
title: Mensagem de EM_EXGETSEL (RichEdit. h)
description: Recupera as posições de caractere inicial e final da seleção em um controle de edição rico.
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- Controles de EM_EXGETSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455439"
---
# <a name="em_exgetsel-message"></a><span data-ttu-id="c3ca0-104">\_Mensagem em EXGETSEL</span><span class="sxs-lookup"><span data-stu-id="c3ca0-104">EM\_EXGETSEL message</span></span>

<span data-ttu-id="c3ca0-105">Recupera as posições de caractere inicial e final da seleção em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="c3ca0-105">Retrieves the starting and ending character positions of the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3ca0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3ca0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ca0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3ca0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3ca0-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c3ca0-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c3ca0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3ca0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3ca0-110">Uma estrutura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que recebe o intervalo de seleção.</span><span class="sxs-lookup"><span data-stu-id="c3ca0-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that receives the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ca0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3ca0-111">Return value</span></span>

<span data-ttu-id="c3ca0-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c3ca0-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ca0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3ca0-113">Requirements</span></span>



| <span data-ttu-id="c3ca0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ca0-114">Requirement</span></span> | <span data-ttu-id="c3ca0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c3ca0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ca0-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3ca0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ca0-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3ca0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3ca0-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3ca0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ca0-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3ca0-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3ca0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3ca0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3ca0-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3ca0-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ca0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3ca0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ca0-123">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="c3ca0-123">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





