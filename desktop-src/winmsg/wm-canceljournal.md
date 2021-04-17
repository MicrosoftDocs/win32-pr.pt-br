---
description: Postado em um aplicativo quando um usuário cancela as atividades de registro em diário do aplicativo. A mensagem é postada com um identificador de janela nulo.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Mensagem de WM_CANCELJOURNAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811656"
---
# <a name="wm_canceljournal-message"></a><span data-ttu-id="99ea6-104">Mensagem do WM \_ CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="99ea6-104">WM\_CANCELJOURNAL message</span></span>

<span data-ttu-id="99ea6-105">Postado em um aplicativo quando um usuário cancela as atividades de registro em diário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99ea6-105">Posted to an application when a user cancels the application's journaling activities.</span></span> <span data-ttu-id="99ea6-106">A mensagem é postada com um identificador de janela **nulo** .</span><span class="sxs-lookup"><span data-stu-id="99ea6-106">The message is posted with a **NULL** window handle.</span></span>


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a><span data-ttu-id="99ea6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99ea6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99ea6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99ea6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99ea6-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="99ea6-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="99ea6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99ea6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99ea6-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="99ea6-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99ea6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99ea6-112">Return value</span></span>

<span data-ttu-id="99ea6-113">Tipo: **void**</span><span class="sxs-lookup"><span data-stu-id="99ea6-113">Type: **void**</span></span>

<span data-ttu-id="99ea6-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="99ea6-114">This message does not return a value.</span></span> <span data-ttu-id="99ea6-115">Ele deve ser processado de dentro do loop principal de um aplicativo ou de um procedimento de gancho [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) , não de um procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="99ea6-115">It is meant to be processed from within an application's main loop or a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) hook procedure, not from a window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="99ea6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="99ea6-116">Remarks</span></span>

<span data-ttu-id="99ea6-117">Os modos de registro e reprodução de diário são modos impostos no sistema que permitem que um aplicativo grave ou reproduza entrada do usuário de forma sequencial.</span><span class="sxs-lookup"><span data-stu-id="99ea6-117">Journal record and playback modes are modes imposed on the system that let an application sequentially record or play back user input.</span></span> <span data-ttu-id="99ea6-118">O sistema entra nesses modos quando um aplicativo instala um procedimento de gancho [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) ou [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="99ea6-118">The system enters these modes when an application installs a [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) or [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) hook procedure.</span></span> <span data-ttu-id="99ea6-119">Quando o sistema está em um desses modos de registro em diário, os aplicativos devem assumir a leitura da entrada da fila de entrada.</span><span class="sxs-lookup"><span data-stu-id="99ea6-119">When the system is in either of these journaling modes, applications must take turns reading input from the input queue.</span></span> <span data-ttu-id="99ea6-120">Se qualquer aplicativo parar de ler a entrada enquanto o sistema estiver em um modo de registro no diário, outros aplicativos serão forçados a aguardar.</span><span class="sxs-lookup"><span data-stu-id="99ea6-120">If any one application stops reading input while the system is in a journaling mode, other applications are forced to wait.</span></span>

<span data-ttu-id="99ea6-121">Para garantir um sistema robusto, que não pode se tornar não responsivo por nenhum aplicativo, o sistema cancela automaticamente todas as atividades do diário quando um usuário pressiona CTRL + ESC ou CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="99ea6-121">To ensure a robust system, one that cannot be made unresponsive by any one application, the system automatically cancels any journaling activities when a user presses CTRL+ESC or CTRL+ALT+DEL.</span></span> <span data-ttu-id="99ea6-122">Em seguida, o sistema desvincula qualquer procedimento de gancho do diário e posta uma mensagem do **WM \_ CANCELJOURNAL** , com um identificador de janela **nulo** , para o aplicativo que define o gancho do diário.</span><span class="sxs-lookup"><span data-stu-id="99ea6-122">The system then unhooks any journaling hook procedures, and posts a **WM\_CANCELJOURNAL** message, with a **NULL** window handle, to the application that set the journaling hook.</span></span>

<span data-ttu-id="99ea6-123">A mensagem do **WM \_ CANCELJOURNAL** tem um identificador de janela **nulo** , portanto, não pode ser expedida para um procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="99ea6-123">The **WM\_CANCELJOURNAL** message has a **NULL** window handle, therefore it cannot be dispatched to a window procedure.</span></span> <span data-ttu-id="99ea6-124">Há duas maneiras de um aplicativo ver uma mensagem do **WM \_ CANCELJOURNAL** : se o aplicativo estiver em execução em seu próprio loop principal, ele deverá capturar a mensagem entre sua chamada para [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) e sua chamada para [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span><span class="sxs-lookup"><span data-stu-id="99ea6-124">There are two ways for an application to see a **WM\_CANCELJOURNAL** message: If the application is running in its own main loop, it must catch the message between its call to [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) and its call to [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="99ea6-125">Se o aplicativo não estiver em execução em seu próprio loop principal, ele deverá definir um procedimento de gancho de [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (por meio de uma chamada para [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) especificando o tipo de gancho do **qu \_ GETMESSAGE** ) que observa a mensagem.</span><span class="sxs-lookup"><span data-stu-id="99ea6-125">If the application is not running in its own main loop, it must set a [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) hook procedure (through a call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) specifying the **WH\_GETMESSAGE** hook type) that watches for the message.</span></span>

<span data-ttu-id="99ea6-126">Quando um aplicativo vê uma mensagem do **WM \_ CANCELJOURNAL** , ele pode assumir duas coisas: o usuário cancelou intencionalmente o registro de diário ou o modo de reprodução, e o sistema já desvinculou nenhum procedimento de registro de diário ou de conexão de reprodução.</span><span class="sxs-lookup"><span data-stu-id="99ea6-126">When an application sees a **WM\_CANCELJOURNAL** message, it can assume two things: the user has intentionally canceled the journal record or playback mode, and the system has already unhooked any journal record or playback hook procedures.</span></span>

<span data-ttu-id="99ea6-127">Observe que as combinações de teclas mencionadas acima (CTRL + ESC ou CTRL + ALT + DEL) fazem com que o sistema cancele o registro no diário.</span><span class="sxs-lookup"><span data-stu-id="99ea6-127">Note that the key combinations mentioned above (CTRL+ESC or CTRL+ALT+DEL) cause the system to cancel journaling.</span></span> <span data-ttu-id="99ea6-128">Se algum aplicativo for desfeito sem resposta, ele dará ao usuário um meio de recuperação.</span><span class="sxs-lookup"><span data-stu-id="99ea6-128">If any one application is made unresponsive, they give the user a means of recovery.</span></span> <span data-ttu-id="99ea6-129">O código de chave virtual [**VK \_ Cancel**](../inputdev/virtual-key-codes.md) (geralmente implementado como a combinação de teclas Ctrl + Break) é o que um aplicativo que está no modo de registro de diário deve observar como um sinal de que o usuário deseja cancelar a atividade de registro em log.</span><span class="sxs-lookup"><span data-stu-id="99ea6-129">The [**VK\_CANCEL**](../inputdev/virtual-key-codes.md) virtual key code (usually implemented as the CTRL+BREAK key combination) is what an application that is in journal record mode should watch for as a signal that the user wishes to cancel the journaling activity.</span></span> <span data-ttu-id="99ea6-130">A diferença é que observar **VK \_ Cancel** é um comportamento sugerido para o registro em log de aplicativos, enquanto CTRL + ESC ou Ctrl + Alt + Del fazem com que o sistema cancele o registro em log, independentemente do comportamento de um aplicativo de registro no diário.</span><span class="sxs-lookup"><span data-stu-id="99ea6-130">The difference is that watching for **VK\_CANCEL** is a suggested behavior for journaling applications, whereas CTRL+ESC or CTRL+ALT+DEL cause the system to cancel journaling regardless of a journaling application's behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="99ea6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99ea6-131">Requirements</span></span>



| <span data-ttu-id="99ea6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="99ea6-132">Requirement</span></span> | <span data-ttu-id="99ea6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="99ea6-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99ea6-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99ea6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="99ea6-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99ea6-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99ea6-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99ea6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="99ea6-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99ea6-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99ea6-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99ea6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="99ea6-139"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99ea6-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99ea6-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="99ea6-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="99ea6-141">**Referência**</span><span class="sxs-lookup"><span data-stu-id="99ea6-141">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="99ea6-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99ea6-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="99ea6-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99ea6-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="99ea6-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="99ea6-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="99ea6-145">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="99ea6-145">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="99ea6-146">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="99ea6-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="99ea6-147">Ganchos</span><span class="sxs-lookup"><span data-stu-id="99ea6-147">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
