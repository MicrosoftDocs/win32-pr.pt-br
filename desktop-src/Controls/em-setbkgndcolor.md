---
title: Mensagem de EM_SETBKGNDCOLOR (RichEdit. h)
description: A \_ mensagem em SETBKGNDCOLOR define a cor do plano de fundo para um controle de edição rico.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- Controles de EM_SETBKGNDCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824688"
---
# <a name="em_setbkgndcolor-message"></a><span data-ttu-id="8121b-104">\_Mensagem em SETBKGNDCOLOR</span><span class="sxs-lookup"><span data-stu-id="8121b-104">EM\_SETBKGNDCOLOR message</span></span>

<span data-ttu-id="8121b-105">A mensagem em **\_ SETBKGNDCOLOR** define a cor do plano de fundo para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="8121b-105">The **EM\_SETBKGNDCOLOR** message sets the background color for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8121b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8121b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8121b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8121b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8121b-108">Especifica se a cor do sistema deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="8121b-108">Specifies whether to use the system color.</span></span> <span data-ttu-id="8121b-109">Se esse parâmetro for um valor diferente de zero, o plano de fundo será definido como a cor do sistema de plano de fundo da janela.</span><span class="sxs-lookup"><span data-stu-id="8121b-109">If this parameter is a nonzero value, the background is set to the window background system color.</span></span> <span data-ttu-id="8121b-110">Caso contrário, o plano de fundo será definido como a cor especificada.</span><span class="sxs-lookup"><span data-stu-id="8121b-110">Otherwise, the background is set to the specified color.</span></span>

</dd> <dt>

<span data-ttu-id="8121b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8121b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8121b-112">Uma estrutura [**COLORREF**](/windows/desktop/gdi/colorref) especificando a cor se *wParam* for zero.</span><span class="sxs-lookup"><span data-stu-id="8121b-112">A [**COLORREF**](/windows/desktop/gdi/colorref) structure specifying the color if *wParam* is zero.</span></span> <span data-ttu-id="8121b-113">Para gerar um **COLORREF**, use a macro [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="8121b-113">To generate a **COLORREF**, use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8121b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8121b-114">Return value</span></span>

<span data-ttu-id="8121b-115">Essa mensagem retorna a cor do plano de fundo original.</span><span class="sxs-lookup"><span data-stu-id="8121b-115">This message returns the original background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="8121b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8121b-116">Requirements</span></span>



| <span data-ttu-id="8121b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8121b-117">Requirement</span></span> | <span data-ttu-id="8121b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8121b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8121b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8121b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8121b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8121b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8121b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8121b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8121b-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8121b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8121b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8121b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8121b-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8121b-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8121b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8121b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8121b-126">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="8121b-126">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8121b-127">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="8121b-127">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> <dt>

[<span data-ttu-id="8121b-128">**RGB**</span><span class="sxs-lookup"><span data-stu-id="8121b-128">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

