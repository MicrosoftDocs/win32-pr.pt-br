---
title: Código de notificação EN_ALIGN_LTR_EC (WinUser. h)
description: Enviado quando o usuário altera a direção do controle de edição para da esquerda para a direita. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de comando do WM \_ .
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- EN_ALIGN_LTR_EC de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4886c68a024005c4b2fddd71e1480b0a3545bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644522"
---
# <a name="en_align_ltr_ec-notification-code"></a><span data-ttu-id="aa227-105">\_Código de \_ notificação do EC-align LTR \_</span><span class="sxs-lookup"><span data-stu-id="aa227-105">EN\_ALIGN\_LTR\_EC notification code</span></span>

<span data-ttu-id="aa227-106">Enviado quando o usuário altera a direção do controle de edição para da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="aa227-106">Sent when the user has changed the edit control direction to left-to-right.</span></span> <span data-ttu-id="aa227-107">A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="aa227-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGN_LTR_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="aa227-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa227-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa227-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa227-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa227-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="aa227-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="aa227-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="aa227-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="aa227-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa227-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa227-113">Um identificador para o controle de edição que envia o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="aa227-113">A handle to the edit control sending the notification code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa227-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa227-114">Remarks</span></span>

<span data-ttu-id="aa227-115">Se houver uma linguagem bidirecional instalada em seu sistema, por exemplo, árabe ou Hebraico, você poderá alterar a direção do controle de edição usando CTRL + LSHIFT (da esquerda para a direita) e CTRL + RSHIFT (da direita para a esquerda).</span><span class="sxs-lookup"><span data-stu-id="aa227-115">If there is a bidirectional language installed on your system, for example, Arabic or Hebrew, you can change the edit control direction using CTRL+LSHIFT (for left to right) and CTRL+RSHIFT (for right to left).</span></span>

<span data-ttu-id="aa227-116">**Edição avançada:** Não há suporte para este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="aa227-116">**Rich Edit:** This notification code is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa227-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa227-117">Requirements</span></span>



| <span data-ttu-id="aa227-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa227-118">Requirement</span></span> | <span data-ttu-id="aa227-119">Valor</span><span class="sxs-lookup"><span data-stu-id="aa227-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa227-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa227-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa227-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa227-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aa227-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa227-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa227-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa227-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="aa227-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa227-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa227-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa227-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa227-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa227-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa227-127">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="aa227-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

