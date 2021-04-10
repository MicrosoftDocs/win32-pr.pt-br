---
description: Enviado quando uma janela está sendo destruída. Ele é enviado para o procedimento de janela da janela que está sendo destruída depois que a janela é removida da tela.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Mensagem de WM_DESTROY (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170448"
---
# <a name="wm_destroy-message"></a><span data-ttu-id="35a7b-104">Mensagem de destruição do WM \_</span><span class="sxs-lookup"><span data-stu-id="35a7b-104">WM\_DESTROY message</span></span>

<span data-ttu-id="35a7b-105">Enviado quando uma janela está sendo destruída.</span><span class="sxs-lookup"><span data-stu-id="35a7b-105">Sent when a window is being destroyed.</span></span> <span data-ttu-id="35a7b-106">Ele é enviado para o procedimento de janela da janela que está sendo destruída depois que a janela é removida da tela.</span><span class="sxs-lookup"><span data-stu-id="35a7b-106">It is sent to the window procedure of the window being destroyed after the window is removed from the screen.</span></span>

<span data-ttu-id="35a7b-107">Essa mensagem é enviada primeiro para a janela que está sendo destruída e, em seguida, para as janelas filhas (se houver) à medida que elas são destruídas.</span><span class="sxs-lookup"><span data-stu-id="35a7b-107">This message is sent first to the window being destroyed and then to the child windows (if any) as they are destroyed.</span></span> <span data-ttu-id="35a7b-108">Durante o processamento da mensagem, pode-se pressupor que todas as janelas filhas ainda existam.</span><span class="sxs-lookup"><span data-stu-id="35a7b-108">During the processing of the message, it can be assumed that all child windows still exist.</span></span>

<span data-ttu-id="35a7b-109">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="35a7b-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a><span data-ttu-id="35a7b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35a7b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a7b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35a7b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35a7b-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="35a7b-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35a7b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35a7b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35a7b-114">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="35a7b-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a7b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35a7b-115">Return value</span></span>

<span data-ttu-id="35a7b-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="35a7b-116">Type: **LRESULT**</span></span>

<span data-ttu-id="35a7b-117">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="35a7b-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a7b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="35a7b-118">Remarks</span></span>

<span data-ttu-id="35a7b-119">Se a janela que está sendo destruída fizer parte da cadeia do Visualizador da área de transferência (definida chamando a função [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), a janela deverá se remover da cadeia processando a função [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) antes de retornar da mensagem do **WM \_ Destroy** .</span><span class="sxs-lookup"><span data-stu-id="35a7b-119">If the window being destroyed is part of the clipboard viewer chain (set by calling the [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) function), the window must remove itself from the chain by processing the [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) function before returning from the **WM\_DESTROY** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a7b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35a7b-120">Requirements</span></span>



| <span data-ttu-id="35a7b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a7b-121">Requirement</span></span> | <span data-ttu-id="35a7b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="35a7b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a7b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35a7b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="35a7b-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="35a7b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="35a7b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35a7b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="35a7b-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="35a7b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35a7b-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="35a7b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="35a7b-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35a7b-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a7b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="35a7b-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="35a7b-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="35a7b-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35a7b-131">**ChangeClipboardChain**</span><span class="sxs-lookup"><span data-stu-id="35a7b-131">**ChangeClipboardChain**</span></span>](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[<span data-ttu-id="35a7b-132">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="35a7b-132">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="35a7b-133">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="35a7b-133">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="35a7b-134">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="35a7b-134">**SetClipboardViewer**</span></span>](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="35a7b-135">**fechar o WM \_**</span><span class="sxs-lookup"><span data-stu-id="35a7b-135">**WM\_CLOSE**</span></span>](wm-close.md)
</dt> <dt>

<span data-ttu-id="35a7b-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="35a7b-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35a7b-137">Windows</span><span class="sxs-lookup"><span data-stu-id="35a7b-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
