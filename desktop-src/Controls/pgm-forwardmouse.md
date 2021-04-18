---
title: Mensagem de PGM_FORWARDMOUSE (commctrl. h)
description: Habilita ou desabilita o encaminhamento do mouse para o controle de pager. Quando o encaminhamento do mouse está habilitado, o controle de pager encaminha \_ as mensagens MOUSEMOVE do WM para a janela contida. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ForwardMouse do pager.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- Controles de PGM_FORWARDMOUSE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756234"
---
# <a name="pgm_forwardmouse-message"></a><span data-ttu-id="b37e5-106">\_Mensagem FORWARDMOUSE do PGM</span><span class="sxs-lookup"><span data-stu-id="b37e5-106">PGM\_FORWARDMOUSE message</span></span>

<span data-ttu-id="b37e5-107">Habilita ou desabilita o encaminhamento do mouse para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="b37e5-107">Enables or disables mouse forwarding for the pager control.</span></span> <span data-ttu-id="b37e5-108">Quando o encaminhamento do mouse está habilitado, o controle de pager encaminha as mensagens [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) para a janela contida.</span><span class="sxs-lookup"><span data-stu-id="b37e5-108">When mouse forwarding is enabled, the pager control forwards [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to the contained window.</span></span> <span data-ttu-id="b37e5-109">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ ForwardMouse do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .</span><span class="sxs-lookup"><span data-stu-id="b37e5-109">You can send this message explicitly or use the [**Pager\_ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b37e5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b37e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b37e5-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b37e5-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b37e5-112">Valor **bool** que determina se o encaminhamento do mouse está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b37e5-112">**BOOL** value that determines if mouse forwarding is enabled or disabled.</span></span> <span data-ttu-id="b37e5-113">Se esse valor for diferente de zero, o encaminhamento do mouse será habilitado.</span><span class="sxs-lookup"><span data-stu-id="b37e5-113">If this value is nonzero, mouse forwarding is enabled.</span></span> <span data-ttu-id="b37e5-114">Se esse valor for zero, o encaminhamento do mouse será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b37e5-114">If this value is zero, mouse forwarding is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="b37e5-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b37e5-115">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b37e5-116">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b37e5-116">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b37e5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b37e5-117">Return value</span></span>

<span data-ttu-id="b37e5-118">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="b37e5-118">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b37e5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b37e5-119">Requirements</span></span>



| <span data-ttu-id="b37e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b37e5-120">Requirement</span></span> | <span data-ttu-id="b37e5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b37e5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b37e5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b37e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b37e5-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b37e5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b37e5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b37e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b37e5-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b37e5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b37e5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b37e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b37e5-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b37e5-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

