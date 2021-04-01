---
title: Mensagem de WM_NOTIFY (WinUser. h)
description: Enviado por um controle comum para sua janela pai quando um evento ocorreu ou o controle requer algumas informações.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- Controles de WM_NOTIFY de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918692"
---
# <a name="wm_notify-message"></a><span data-ttu-id="737fb-104">Mensagem de notificação do WM \_</span><span class="sxs-lookup"><span data-stu-id="737fb-104">WM\_NOTIFY message</span></span>

<span data-ttu-id="737fb-105">Enviado por um controle comum para sua janela pai quando um evento ocorreu ou o controle requer algumas informações.</span><span class="sxs-lookup"><span data-stu-id="737fb-105">Sent by a common control to its parent window when an event has occurred or the control requires some information.</span></span>

## <a name="parameters"></a><span data-ttu-id="737fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="737fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737fb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="737fb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="737fb-108">O identificador do controle comum que envia a mensagem.</span><span class="sxs-lookup"><span data-stu-id="737fb-108">The identifier of the common control sending the message.</span></span> <span data-ttu-id="737fb-109">Não há garantia de que esse identificador seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="737fb-109">This identifier is not guaranteed to be unique.</span></span> <span data-ttu-id="737fb-110">Um aplicativo deve usar o membro **hwndFrom** ou **IdFrom** da estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (passada como o parâmetro *lParam* ) para identificar o controle.</span><span class="sxs-lookup"><span data-stu-id="737fb-110">An application should use the **hwndFrom** or **idFrom** member of the [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure (passed as the *lParam* parameter) to identify the control.</span></span>

</dd> <dt>

<span data-ttu-id="737fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="737fb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="737fb-112">Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém o código de notificação e informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="737fb-112">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains the notification code and additional information.</span></span> <span data-ttu-id="737fb-113">Para algumas mensagens de notificação, esse parâmetro aponta para uma estrutura maior que tem a estrutura **NMHDR** como seu primeiro membro.</span><span class="sxs-lookup"><span data-stu-id="737fb-113">For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737fb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="737fb-114">Return value</span></span>

<span data-ttu-id="737fb-115">O valor de retorno é ignorado, exceto pelas mensagens de notificação que especificam o contrário.</span><span class="sxs-lookup"><span data-stu-id="737fb-115">The return value is ignored except for notification messages that specify otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="737fb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="737fb-116">Remarks</span></span>

<span data-ttu-id="737fb-117">O destino da mensagem deve ser o **HWND** do pai do controle.</span><span class="sxs-lookup"><span data-stu-id="737fb-117">The destination of the message must be the **HWND** of the parent of the control.</span></span> <span data-ttu-id="737fb-118">Esse valor pode ser obtido usando [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), conforme mostrado no exemplo a seguir, em que *m \_ controlHwnd* é o **HWND** do próprio controle.</span><span class="sxs-lookup"><span data-stu-id="737fb-118">This value can be obtained by using [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), as shown in the following example, where *m\_controlHwnd* is the **HWND** of the control itself.</span></span>


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



<span data-ttu-id="737fb-119">Os aplicativos manipulam a mensagem no procedimento de janela da janela pai, conforme mostrado no exemplo a seguir, que manipula a mensagem de notificação enviada pelo controle personalizado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="737fb-119">Applications handle the message in the window procedure of the parent window, as shown in the following example, which handles the notification message sent by the custom control in the previous example.</span></span>


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



<span data-ttu-id="737fb-120">Algumas notificações, principalmente as que estiveram na API há muito tempo, são enviadas como mensagens de comando do [**WM \_**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="737fb-120">Some notifications, chiefly those that have been in the API for a long time, are sent as [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="737fb-121">Para obter mais informações, consulte [Control messages](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="737fb-121">For more information, see [Control Messages](control-messages.md).</span></span>

<span data-ttu-id="737fb-122">Se o manipulador de mensagens estiver em um procedimento de caixa de diálogo, você deverá usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com DWL \_ MSGRESULT para definir um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="737fb-122">If the message handler is in a dialog box procedure, you must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set a return value.</span></span>

<span data-ttu-id="737fb-123">Para sistemas Windows Vista e posteriores, a mensagem de **\_ notificação do WM** não pode ser enviada entre processos.</span><span class="sxs-lookup"><span data-stu-id="737fb-123">For Windows Vista and later systems, the **WM\_NOTIFY** message cannot be sent between processes.</span></span>

<span data-ttu-id="737fb-124">Muitas notificações estão disponíveis nos formatos ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="737fb-124">Many notifications are available in both ANSI and Unicode formats.</span></span> <span data-ttu-id="737fb-125">A janela que envia a mensagem de **\_ notificação do WM** usa a mensagem do [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) para determinar qual formato deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="737fb-125">The window sending the **WM\_NOTIFY** message uses the [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message to determine which format should be used.</span></span> <span data-ttu-id="737fb-126">Consulte o **WM \_ NOTIFYFORMAT** para mais discussões.</span><span class="sxs-lookup"><span data-stu-id="737fb-126">See **WM\_NOTIFYFORMAT** for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="737fb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="737fb-127">Requirements</span></span>



| <span data-ttu-id="737fb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="737fb-128">Requirement</span></span> | <span data-ttu-id="737fb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="737fb-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="737fb-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="737fb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="737fb-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="737fb-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="737fb-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="737fb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="737fb-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="737fb-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="737fb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="737fb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="737fb-135"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="737fb-135"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="737fb-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="737fb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737fb-137">**NOTIFYFORMAT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="737fb-137">**WM\_NOTIFYFORMAT**</span></span>](wm-notifyformat.md)
</dt> </dl>

 

