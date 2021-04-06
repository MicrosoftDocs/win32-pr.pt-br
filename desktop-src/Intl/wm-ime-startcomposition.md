---
description: Enviado imediatamente antes de o IME gerar a cadeia de caracteres de composição como resultado de um pressionamento de tecla. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: Mensagem de WM_IME_STARTCOMPOSITION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827153"
---
# <a name="wm_ime_startcomposition-message"></a><span data-ttu-id="7fa66-104">\_Mensagem de STARTCOMPOSITION IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="7fa66-104">WM\_IME\_STARTCOMPOSITION message</span></span>

<span data-ttu-id="7fa66-105">Enviado imediatamente antes de o IME gerar a cadeia de caracteres de composição como resultado de um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="7fa66-105">Sent immediately before the IME generates the composition string as a result of a keystroke.</span></span> <span data-ttu-id="7fa66-106">Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7fa66-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="7fa66-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fa66-107">Parameters</span></span>

<span data-ttu-id="7fa66-108">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7fa66-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="7fa66-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fa66-109">Return value</span></span>

<span data-ttu-id="7fa66-110">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="7fa66-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fa66-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fa66-111">Remarks</span></span>

<span data-ttu-id="7fa66-112">Essa mensagem é uma notificação para uma janela do IME para abrir sua janela de composição.</span><span class="sxs-lookup"><span data-stu-id="7fa66-112">This message is a notification to an IME window to open its composition window.</span></span> <span data-ttu-id="7fa66-113">Um aplicativo deve processar essa mensagem se exibir os próprios caracteres de composição.</span><span class="sxs-lookup"><span data-stu-id="7fa66-113">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="7fa66-114">Se um aplicativo tiver criado uma janela IME, ele deverá passar essa mensagem para essa janela.</span><span class="sxs-lookup"><span data-stu-id="7fa66-114">If an application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="7fa66-115">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processa a mensagem passando-a para a janela padrão do IME.</span><span class="sxs-lookup"><span data-stu-id="7fa66-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes the message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fa66-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fa66-116">Requirements</span></span>



| <span data-ttu-id="7fa66-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fa66-117">Requirement</span></span> | <span data-ttu-id="7fa66-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7fa66-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa66-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fa66-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7fa66-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7fa66-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7fa66-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fa66-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7fa66-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7fa66-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7fa66-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7fa66-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fa66-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7fa66-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fa66-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fa66-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fa66-126">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="7fa66-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="7fa66-127">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="7fa66-127">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
