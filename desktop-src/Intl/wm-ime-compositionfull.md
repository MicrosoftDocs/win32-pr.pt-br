---
description: Enviado a um aplicativo quando a janela do IME não encontra espaço para estender a área para a janela de composição. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Mensagem de WM_IME_COMPOSITIONFULL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172171"
---
# <a name="wm_ime_compositionfull-message"></a><span data-ttu-id="d5549-104">\_Mensagem de COMPOSITIONFULL IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="d5549-104">WM\_IME\_COMPOSITIONFULL message</span></span>

<span data-ttu-id="d5549-105">Enviado a um aplicativo quando a janela do IME não encontra espaço para estender a área para a janela de composição.</span><span class="sxs-lookup"><span data-stu-id="d5549-105">Sent to an application when the IME window finds no space to extend the area for the composition window.</span></span> <span data-ttu-id="d5549-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d5549-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="d5549-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5549-107">Parameters</span></span>

<span data-ttu-id="d5549-108">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d5549-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="d5549-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5549-109">Return value</span></span>

<span data-ttu-id="d5549-110">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d5549-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5549-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5549-111">Remarks</span></span>

<span data-ttu-id="d5549-112">O aplicativo deve usar o [comando \_ SETCOMPOSITIONWINDOW do IMC](imc-setcompositionwindow.md) para especificar como a janela deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="d5549-112">The application should use the [IMC\_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) command to specify how the window should be displayed.</span></span>

<span data-ttu-id="d5549-113">A janela do IME, em vez do IME, envia essa mensagem de notificação pela função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="d5549-113">The IME window, instead of the IME, sends this notification message by the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5549-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5549-114">Requirements</span></span>



| <span data-ttu-id="d5549-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5549-115">Requirement</span></span> | <span data-ttu-id="d5549-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d5549-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5549-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5549-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d5549-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d5549-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d5549-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5549-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d5549-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d5549-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5549-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d5549-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5549-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5549-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5549-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5549-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5549-124">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d5549-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d5549-125">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="d5549-125">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="d5549-126">SETCOMPOSITIONWINDOW do IMC \_</span><span class="sxs-lookup"><span data-stu-id="d5549-126">IMC\_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> </dl>

 

 
