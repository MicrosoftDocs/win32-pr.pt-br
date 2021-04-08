---
title: Mensagem de EM_SETHYPHENATEINFO (RichEdit. h)
description: Define a maneira como um controle de edição rico faz a hifenização.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- Controles de EM_SETHYPHENATEINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824686"
---
# <a name="em_sethyphenateinfo-message"></a><span data-ttu-id="52f85-104">\_Mensagem em SETHYPHENATEINFO</span><span class="sxs-lookup"><span data-stu-id="52f85-104">EM\_SETHYPHENATEINFO message</span></span>

<span data-ttu-id="52f85-105">Define a maneira como um controle de edição rico faz a hifenização.</span><span class="sxs-lookup"><span data-stu-id="52f85-105">Sets the way a rich edit control does hyphenation.</span></span>

## <a name="parameters"></a><span data-ttu-id="52f85-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52f85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52f85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52f85-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52f85-108">Ponteiro para uma estrutura [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .</span><span class="sxs-lookup"><span data-stu-id="52f85-108">Pointer to a [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="52f85-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52f85-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52f85-110">Não usado, deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="52f85-110">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52f85-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="52f85-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52f85-112">Para habilitar a hifenização, o cliente deve chamar em [**\_ settipografiaoptions**](em-settypographyoptions.md), especificando para \_ ADVANCEDTYPOGRAPHY.</span><span class="sxs-lookup"><span data-stu-id="52f85-112">To enable hyphenation, the client must call [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md), specifying TO\_ADVANCEDTYPOGRAPHY.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52f85-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52f85-113">Requirements</span></span>



| <span data-ttu-id="52f85-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f85-114">Requirement</span></span> | <span data-ttu-id="52f85-115">Valor</span><span class="sxs-lookup"><span data-stu-id="52f85-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52f85-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52f85-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52f85-117">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="52f85-117">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52f85-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52f85-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52f85-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52f85-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52f85-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52f85-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f85-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f85-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f85-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="52f85-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f85-123">**em \_ GETHYPHENATEINFO**</span><span class="sxs-lookup"><span data-stu-id="52f85-123">**EM\_GETHYPHENATEINFO**</span></span>](em-gethyphenateinfo.md)
</dt> </dl>

 

 





