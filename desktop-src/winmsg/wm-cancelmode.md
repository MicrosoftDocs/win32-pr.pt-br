---
description: Enviado para cancelar determinados modos, como captura do mouse.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Mensagem de WM_CANCELMODE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807844"
---
# <a name="wm_cancelmode-message"></a><span data-ttu-id="b7e25-103">\_Mensagem de cancelamento do WM</span><span class="sxs-lookup"><span data-stu-id="b7e25-103">WM\_CANCELMODE message</span></span>

<span data-ttu-id="b7e25-104">Enviado para cancelar determinados modos, como captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="b7e25-104">Sent to cancel certain modes, such as mouse capture.</span></span> <span data-ttu-id="b7e25-105">Por exemplo, o sistema envia essa mensagem para a janela ativa quando uma caixa de diálogo ou caixa de mensagem é exibida.</span><span class="sxs-lookup"><span data-stu-id="b7e25-105">For example, the system sends this message to the active window when a dialog box or message box is displayed.</span></span> <span data-ttu-id="b7e25-106">Determinadas funções também enviam essa mensagem explicitamente para a janela especificada, independentemente de ser a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="b7e25-106">Certain functions also send this message explicitly to the specified window regardless of whether it is the active window.</span></span> <span data-ttu-id="b7e25-107">Por exemplo, a função [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) envia essa mensagem ao desabilitar a janela especificada.</span><span class="sxs-lookup"><span data-stu-id="b7e25-107">For example, the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function sends this message when disabling the specified window.</span></span>

<span data-ttu-id="b7e25-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b7e25-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CANCELMODE                   0x001F
```



## <a name="parameters"></a><span data-ttu-id="b7e25-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7e25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7e25-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7e25-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7e25-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="b7e25-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b7e25-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7e25-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7e25-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="b7e25-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7e25-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7e25-114">Return value</span></span>

<span data-ttu-id="b7e25-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b7e25-115">Type: **LRESULT**</span></span>

<span data-ttu-id="b7e25-116">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="b7e25-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7e25-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7e25-117">Remarks</span></span>

<span data-ttu-id="b7e25-118">Quando a mensagem de **\_ cancelamento do WM** é enviada, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) cancela o processamento interno da entrada da barra de rolagem padrão, cancela o processamento do menu interno e libera a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="b7e25-118">When the **WM\_CANCELMODE** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function cancels internal processing of standard scroll bar input, cancels internal menu processing, and releases the mouse capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e25-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7e25-119">Requirements</span></span>



| <span data-ttu-id="b7e25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e25-120">Requirement</span></span> | <span data-ttu-id="b7e25-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b7e25-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e25-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7e25-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e25-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b7e25-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b7e25-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7e25-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e25-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b7e25-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b7e25-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b7e25-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e25-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7e25-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7e25-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7e25-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7e25-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b7e25-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b7e25-130">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b7e25-130">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b7e25-131">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="b7e25-131">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[<span data-ttu-id="b7e25-132">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="b7e25-132">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

<span data-ttu-id="b7e25-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b7e25-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b7e25-134">Windows</span><span class="sxs-lookup"><span data-stu-id="b7e25-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
