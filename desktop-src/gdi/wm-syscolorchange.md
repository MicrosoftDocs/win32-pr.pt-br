---
description: A mensagem do WM \_ SYSCOLORCHANGE é enviada para todas as janelas de nível superior quando uma alteração é feita em uma configuração de cor do sistema.
ms.assetid: ffe61768-86d6-4ea8-ae2d-1095a9afa925
title: Mensagem de WM_SYSCOLORCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3883f0534d91a6d852b0e70fbb4edabdcab56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968210"
---
# <a name="wm_syscolorchange-message"></a><span data-ttu-id="ba097-103">Mensagem do WM \_ SYSCOLORCHANGE</span><span class="sxs-lookup"><span data-stu-id="ba097-103">WM\_SYSCOLORCHANGE message</span></span>

<span data-ttu-id="ba097-104">A mensagem do **WM \_ SYSCOLORCHANGE** é enviada para todas as janelas de nível superior quando uma alteração é feita em uma configuração de cor do sistema.</span><span class="sxs-lookup"><span data-stu-id="ba097-104">The **WM\_SYSCOLORCHANGE** message is sent to all top-level windows when a change is made to a system color setting.</span></span>

<span data-ttu-id="ba097-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ba097-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="ba097-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba097-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba097-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba097-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba097-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ba097-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ba097-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba097-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba097-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ba097-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba097-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba097-111">Remarks</span></span>

<span data-ttu-id="ba097-112">O sistema envia uma mensagem de [**\_ pintura do WM**](wm-paint.md) para qualquer janela afetada por uma alteração de cor do sistema.</span><span class="sxs-lookup"><span data-stu-id="ba097-112">The system sends a [**WM\_PAINT**](wm-paint.md) message to any window that is affected by a system color change.</span></span>

<span data-ttu-id="ba097-113">Os aplicativos que têm pincéis usando as cores do sistema existentes devem excluir esses pincéis e recriá-los usando as novas cores do sistema.</span><span class="sxs-lookup"><span data-stu-id="ba097-113">Applications that have brushes using the existing system colors should delete those brushes and re-create them using the new system colors.</span></span>

<span data-ttu-id="ba097-114">As janelas de nível superior que usam controles comuns devem encaminhar a mensagem do **WM \_ SYSCOLORCHANGE** para os controles; caso contrário, os controles não serão notificados sobre a alteração de cor.</span><span class="sxs-lookup"><span data-stu-id="ba097-114">Top level windows that use common controls must forward the **WM\_SYSCOLORCHANGE** message to the controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="ba097-115">Isso garante que as cores usadas por seus controles comuns sejam consistentes com as usadas por outros objetos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ba097-115">This ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="ba097-116">Por exemplo, um controle Toolbar usa a cor "objetos 3D" para desenhar seus botões.</span><span class="sxs-lookup"><span data-stu-id="ba097-116">For example, a toolbar control uses the "3D Objects" color to draw its buttons.</span></span> <span data-ttu-id="ba097-117">Se o usuário alterar a cor dos objetos 3D, mas a mensagem do **WM \_ SYSCOLORCHANGE** não for encaminhada para a barra de ferramentas, os botões da barra de ferramentas permanecerão na cor original, enquanto a cor de outros botões no sistema será alterada.</span><span class="sxs-lookup"><span data-stu-id="ba097-117">If the user changes the 3D Objects color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color while the color of other buttons in the system changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba097-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba097-118">Requirements</span></span>



| <span data-ttu-id="ba097-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba097-119">Requirement</span></span> | <span data-ttu-id="ba097-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ba097-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba097-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba097-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba097-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba097-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ba097-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba097-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba097-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba097-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ba097-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ba097-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba097-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba097-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba097-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba097-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba097-128">Visão geral das cores</span><span class="sxs-lookup"><span data-stu-id="ba097-128">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="ba097-129">Mensagens de cores</span><span class="sxs-lookup"><span data-stu-id="ba097-129">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="ba097-130">**pintura do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ba097-130">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
