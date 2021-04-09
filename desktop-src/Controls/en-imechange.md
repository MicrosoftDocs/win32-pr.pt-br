---
title: EN_IMECHANGE código de notificação (RichEdit. h)
description: Notifica um pai do controle de edição rico de que o status de conversão do IME foi alterado.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009401"
---
# <a name="en_imechange-notification-code"></a><span data-ttu-id="d273c-104">\_Código de notificação en IMECHANGE</span><span class="sxs-lookup"><span data-stu-id="d273c-104">EN\_IMECHANGE notification code</span></span>

<span data-ttu-id="d273c-105">Notifica um pai do controle de edição rico de que o status de conversão do IME foi alterado.</span><span class="sxs-lookup"><span data-stu-id="d273c-105">Notifies a rich edit control's parent that the IME conversion status has changed.</span></span> <span data-ttu-id="d273c-106">Esse código de notificação está disponível *apenas* para versões em idiomas asiáticos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d273c-106">This notification code is available *only* for Asian-language versions of the operating system.</span></span> <span data-ttu-id="d273c-107">Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d273c-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d273c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d273c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d273c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d273c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d273c-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="d273c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="d273c-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="d273c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d273c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d273c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d273c-113">Manipular para o controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="d273c-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d273c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d273c-114">Return value</span></span>

<span data-ttu-id="d273c-115">Esse código de notificação retorna zero.</span><span class="sxs-lookup"><span data-stu-id="d273c-115">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d273c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d273c-116">Remarks</span></span>

<span data-ttu-id="d273c-117">Para receber \_ códigos de notificação do en IMECHANGE, especifique [**enm \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d273c-117">To receive EN\_IMECHANGE notification codes, specify [**ENM\_IMECHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="d273c-118">Esse código de notificação só tem suporte na versão asiática do Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="d273c-118">This notification code is only supported in the Asian version of Rich Edit 1.0.</span></span> <span data-ttu-id="d273c-119">Não há suporte para ele em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d273c-119">It is not supported in later versions.</span></span> <span data-ttu-id="d273c-120">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d273c-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d273c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d273c-121">Requirements</span></span>



| <span data-ttu-id="d273c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d273c-122">Requirement</span></span> | <span data-ttu-id="d273c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d273c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d273c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d273c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d273c-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d273c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d273c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d273c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d273c-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d273c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d273c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d273c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d273c-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d273c-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d273c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d273c-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="d273c-131">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="d273c-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d273c-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d273c-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d273c-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d273c-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d273c-134">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d273c-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

