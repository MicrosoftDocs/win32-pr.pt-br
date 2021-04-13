---
title: Mensagem de TTM_RELAYEVENT (commctrl. h)
description: Passa uma mensagem do mouse para um controle ToolTip para processamento.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- Controles de TTM_RELAYEVENT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298299"
---
# <a name="ttm_relayevent-message"></a><span data-ttu-id="a0292-104">\_Mensagem TTM RELAYEVENT</span><span class="sxs-lookup"><span data-stu-id="a0292-104">TTM\_RELAYEVENT message</span></span>

<span data-ttu-id="a0292-105">Passa uma mensagem do mouse para um controle ToolTip para processamento.</span><span class="sxs-lookup"><span data-stu-id="a0292-105">Passes a mouse message to a tooltip control for processing.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0292-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0292-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0292-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0292-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0292-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a0292-108">Must be zero.</span></span> <span data-ttu-id="a0292-109">**Windows 7 e posterior:** Se a posição da dica de ferramenta for deslocada da posição do cursor (na ordem não ser obstruída por um dedo ou um dispositivo apontador), esse parâmetro poderá conter informações extras da mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="a0292-109">**Windows 7 and later:** If the position of the tooltip is offset from the cursor position (in order not be obstructed by a finger or pointing device), this parameter can contain extra information taken from the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="a0292-110">Recupere essas informações extras com [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span><span class="sxs-lookup"><span data-stu-id="a0292-110">Retrieve this extra information with [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span></span>

</dd> <dt>

<span data-ttu-id="a0292-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0292-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0292-112">Ponteiro para uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) que contém a mensagem a ser retransmitida.</span><span class="sxs-lookup"><span data-stu-id="a0292-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to relay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0292-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0292-113">Return value</span></span>

<span data-ttu-id="a0292-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a0292-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0292-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0292-115">Remarks</span></span>

<span data-ttu-id="a0292-116">Um controle ToolTip processa apenas as seguintes mensagens passadas para ele pela mensagem **TTM \_ RELAYEVENT** :</span><span class="sxs-lookup"><span data-stu-id="a0292-116">A tooltip control processes only the following messages passed to it by the **TTM\_RELAYEVENT** message:</span></span>

-   <span data-ttu-id="a0292-117">LBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="a0292-117">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="a0292-118">LBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="a0292-118">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="a0292-119">MBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="a0292-119">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="a0292-120">MBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="a0292-120">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="a0292-121">admousemove do WM \_</span><span class="sxs-lookup"><span data-stu-id="a0292-121">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="a0292-122">NCMOUSEMOVE do WM \_</span><span class="sxs-lookup"><span data-stu-id="a0292-122">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="a0292-123">RBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="a0292-123">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="a0292-124">RBUTTONUP do WM \_</span><span class="sxs-lookup"><span data-stu-id="a0292-124">WM\_RBUTTONUP</span></span>

<span data-ttu-id="a0292-125">Todas as outras mensagens são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="a0292-125">All other messages are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0292-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0292-126">Requirements</span></span>



| <span data-ttu-id="a0292-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0292-127">Requirement</span></span> | <span data-ttu-id="a0292-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a0292-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0292-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0292-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a0292-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0292-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0292-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0292-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a0292-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0292-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0292-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0292-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0292-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0292-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

