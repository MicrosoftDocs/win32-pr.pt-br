---
description: Não executa nenhuma operação. Um aplicativo enviará a \_ mensagem nula do WM se quiser postar uma mensagem que a janela do destinatário ignorará.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Mensagem de WM_NULL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169531"
---
# <a name="wm_null-message"></a><span data-ttu-id="58568-104">\_Mensagem nula do WM</span><span class="sxs-lookup"><span data-stu-id="58568-104">WM\_NULL message</span></span>

<span data-ttu-id="58568-105">Não executa nenhuma operação.</span><span class="sxs-lookup"><span data-stu-id="58568-105">Performs no operation.</span></span> <span data-ttu-id="58568-106">Um aplicativo enviará a mensagem **\_ nula do WM** se quiser postar uma mensagem que a janela do destinatário ignorará.</span><span class="sxs-lookup"><span data-stu-id="58568-106">An application sends the **WM\_NULL** message if it wants to post a message that the recipient window will ignore.</span></span>

<span data-ttu-id="58568-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="58568-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a><span data-ttu-id="58568-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58568-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58568-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58568-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58568-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="58568-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58568-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58568-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58568-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="58568-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58568-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58568-113">Return value</span></span>

<span data-ttu-id="58568-114">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="58568-114">Type: **LRESULT**</span></span>

<span data-ttu-id="58568-115">Um aplicativo retornará zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="58568-115">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="58568-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="58568-116">Remarks</span></span>

<span data-ttu-id="58568-117">Por exemplo, se um aplicativo tiver instalado um gancho de **qu \_** e quiser impedir que uma mensagem seja processada, a função de retorno de chamada [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) poderá alterar o número da mensagem para o **WM \_ NULL** para que o destinatário o ignore.</span><span class="sxs-lookup"><span data-stu-id="58568-117">For example, if an application has installed a **WH\_GETMESSAGE** hook and wants to prevent a message from being processed, the [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) callback function can change the message number to **WM\_NULL** so the recipient will ignore it.</span></span>

<span data-ttu-id="58568-118">Como outro exemplo, um aplicativo pode verificar se uma janela está respondendo às mensagens enviando a **mensagem \_ nula do WM** com a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="58568-118">As another example, an application can check if a window is responding to messages by sending the **WM\_NULL** message with the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="58568-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58568-119">Requirements</span></span>



| <span data-ttu-id="58568-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="58568-120">Requirement</span></span> | <span data-ttu-id="58568-121">Valor</span><span class="sxs-lookup"><span data-stu-id="58568-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58568-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58568-122">Minimum supported client</span></span><br/> | <span data-ttu-id="58568-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58568-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="58568-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58568-124">Minimum supported server</span></span><br/> | <span data-ttu-id="58568-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58568-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58568-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="58568-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="58568-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58568-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58568-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="58568-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58568-129">Visão geral do Windows</span><span class="sxs-lookup"><span data-stu-id="58568-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
