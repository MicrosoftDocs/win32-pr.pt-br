---
title: EN_LINK código de notificação (RichEdit. h)
description: Um controle de edição rico envia \_ códigos de notificação de link quando recebe várias mensagens, por exemplo, quando o usuário clica no mouse ou quando o ponteiro do mouse está sobre o texto que tem o \_ efeito de link CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- EN_LINK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455759"
---
# <a name="en_link-notification-code"></a><span data-ttu-id="d55cf-104">\_Código de notificação do link en</span><span class="sxs-lookup"><span data-stu-id="d55cf-104">EN\_LINK notification code</span></span>

<span data-ttu-id="d55cf-105">Um controle de edição rico envia \_ códigos de notificação de link quando recebe várias mensagens, por exemplo, quando o usuário clica no mouse ou quando o ponteiro do mouse está sobre o texto que tem o efeito de **\_ link CFE** .</span><span class="sxs-lookup"><span data-stu-id="d55cf-105">A rich edit control sends EN\_LINK notification codes when it receives various messages, for example, when the user clicks the mouse or when the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="d55cf-106">Um controle de edição rico sem janela envia essa notificação usando o método [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="d55cf-106">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span> <span data-ttu-id="d55cf-107">A janela pai do controle recebe esse código de notificação por meio de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d55cf-107">The parent window of the control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d55cf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d55cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d55cf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d55cf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d55cf-110">A ID da janela recuperada chamando a função [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o \_ valor da ID GWL.</span><span class="sxs-lookup"><span data-stu-id="d55cf-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="d55cf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d55cf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d55cf-112">Ponteiro para uma estrutura de [**ENlinks**](/windows/desktop/api/Richedit/ns-richedit-enlink) .</span><span class="sxs-lookup"><span data-stu-id="d55cf-112">Pointer to an [**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink) structure.</span></span> <span data-ttu-id="d55cf-113">A estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , informações sobre o código de notificação e uma estrutura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que indica o intervalo de caracteres que têm o efeito de **\_ link CFE** .</span><span class="sxs-lookup"><span data-stu-id="d55cf-113">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, information about the notification code, and a [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that indicates the range of characters that have the **CFE\_LINK** effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d55cf-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d55cf-114">Return value</span></span>

<span data-ttu-id="d55cf-115">Retorna zero para permitir que o controle prossiga com seu tratamento normal da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d55cf-115">Return zero to allow the control to proceed with its normal handling of the message.</span></span>

<span data-ttu-id="d55cf-116">Retornar um valor diferente de zero para impedir que o controle trate a mensagem.</span><span class="sxs-lookup"><span data-stu-id="d55cf-116">Return a nonzero value to prevent the control from handling the message.</span></span>

<span data-ttu-id="d55cf-117">**Windows 8**: retornar **link en, por \_ \_ \_ padrão** , para direcionar o controle de edição rico para executar a ação padrão.</span><span class="sxs-lookup"><span data-stu-id="d55cf-117">**Windows 8**: Return **EN\_LINK\_DO\_DEFAULT** to direct the rich edit control to perform the default action.</span></span>

## <a name="remarks"></a><span data-ttu-id="d55cf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d55cf-118">Remarks</span></span>

<span data-ttu-id="d55cf-119">Para receber códigos de notificação de **\_ link** quando o link tiver foco, especifique o sinalizador de [**\_ link enm**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d55cf-119">To receive **EN\_LINK** notification codes when the link has focus, specify the [**ENM\_LINK**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="d55cf-120">Se o link não tiver foco, para receber os códigos de notificação de **\_ link** , especifique o sinalizador **\_ NOFOCUSLINKNOTIFY do ses** na máscara enviada com a mensagem em [**\_ seteditstyle**](em-seteditstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="d55cf-120">If the link has no focus, to receive **EN\_LINK** notification codes specify the **SES\_NOFOCUSLINKNOTIFY** flag in the mask sent with the [**EM\_SETEDITSTYLE**](em-seteditstyle.md) message.</span></span>

<span data-ttu-id="d55cf-121">Um controle rich edit envia códigos de notificação de **\_ link** quando recebe as seguintes mensagens enquanto o ponteiro do mouse está sobre o texto que tem o efeito de **\_ link CFE** :</span><span class="sxs-lookup"><span data-stu-id="d55cf-121">A rich edit control sends **EN\_LINK** notification codes when it receives the following messages while the mouse pointer is over text that has the **CFE\_LINK** effect:</span></span>

-   [<span data-ttu-id="d55cf-122">**LBUTTONDBLCLK do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d55cf-122">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [<span data-ttu-id="d55cf-123">**LBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d55cf-123">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)
-   [<span data-ttu-id="d55cf-124">**LBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d55cf-124">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)
-   [<span data-ttu-id="d55cf-125">**admousemove do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d55cf-125">**WM\_MOUSEMOVE**</span></span>](/windows/desktop/inputdev/wm-mousemove)
-   [<span data-ttu-id="d55cf-126">**RBUTTONDBLCLK do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d55cf-126">**WM\_RBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [<span data-ttu-id="d55cf-127">**RBUTTONDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d55cf-127">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown)
-   [<span data-ttu-id="d55cf-128">**RBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d55cf-128">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
-   [<span data-ttu-id="d55cf-129">**WM \_ SETcursor**</span><span class="sxs-lookup"><span data-stu-id="d55cf-129">**WM\_SETCURSOR**</span></span>](/windows/desktop/menurc/wm-setcursor)

<span data-ttu-id="d55cf-130">O efeito de **\_ link do CFE** normalmente identifica um intervalo de texto que contém uma URL.</span><span class="sxs-lookup"><span data-stu-id="d55cf-130">The **CFE\_LINK** effect typically identifies a range of text that contains an URL.</span></span> <span data-ttu-id="d55cf-131">Os aplicativos podem manipular o \_ código de notificação do link en alterando o ponteiro do mouse quando ele está sobre a URL ou iniciando um navegador para exibir o local identificado pela URL.</span><span class="sxs-lookup"><span data-stu-id="d55cf-131">Applications can handle the EN\_LINK notification code by changing the mouse pointer when it is over the URL, or by starting a browser to view the location identified by the URL.</span></span>

<span data-ttu-id="d55cf-132">Se você enviar a mensagem em [**\_ AUTOURLDETECT**](em-autourldetect.md) para habilitar a detecção automática de URL, o controle de edição rico definirá automaticamente o efeito de **\_ link CFE** para o texto modificado que ele identifica como uma URL.</span><span class="sxs-lookup"><span data-stu-id="d55cf-132">If you send the [**EM\_AUTOURLDETECT**](em-autourldetect.md) message to enable automatic URL detection, the rich edit control automatically sets the **CFE\_LINK** effect for modified text that it identifies as a URL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d55cf-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d55cf-133">Requirements</span></span>



| <span data-ttu-id="d55cf-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d55cf-134">Requirement</span></span> | <span data-ttu-id="d55cf-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d55cf-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d55cf-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d55cf-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d55cf-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d55cf-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d55cf-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d55cf-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d55cf-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d55cf-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d55cf-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d55cf-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d55cf-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d55cf-141"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d55cf-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d55cf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55cf-143">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="d55cf-143">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[<span data-ttu-id="d55cf-144">**em \_ AUTOURLDETECT**</span><span class="sxs-lookup"><span data-stu-id="d55cf-144">**EM\_AUTOURLDETECT**</span></span>](em-autourldetect.md)
</dt> <dt>

[<span data-ttu-id="d55cf-145">**VINCULAR**</span><span class="sxs-lookup"><span data-stu-id="d55cf-145">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[<span data-ttu-id="d55cf-146">**ITextRange2:: SetURL**</span><span class="sxs-lookup"><span data-stu-id="d55cf-146">**ITextRange2::SetURL**</span></span>](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[<span data-ttu-id="d55cf-147">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="d55cf-147">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

