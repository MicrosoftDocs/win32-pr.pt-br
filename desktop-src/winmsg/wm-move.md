---
description: Enviado após uma janela ser movida.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Mensagem de WM_MOVE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770048"
---
# <a name="wm_move-message"></a><span data-ttu-id="483cd-103">Mensagem de movimentação do WM \_</span><span class="sxs-lookup"><span data-stu-id="483cd-103">WM\_MOVE message</span></span>

<span data-ttu-id="483cd-104">Enviado após uma janela ser movida.</span><span class="sxs-lookup"><span data-stu-id="483cd-104">Sent after a window has been moved.</span></span>

<span data-ttu-id="483cd-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="483cd-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a><span data-ttu-id="483cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="483cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="483cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="483cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="483cd-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="483cd-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="483cd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="483cd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="483cd-110">As coordenadas x e y do canto superior esquerdo da área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="483cd-110">The x and y coordinates of the upper-left corner of the client area of the window.</span></span> <span data-ttu-id="483cd-111">A palavra de ordem inferior contém a coordenada x, enquanto a palavra de ordem superior contém a coordenada y.</span><span class="sxs-lookup"><span data-stu-id="483cd-111">The low-order word contains the x-coordinate while the high-order word contains the y coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="483cd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="483cd-112">Return value</span></span>

<span data-ttu-id="483cd-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="483cd-113">Type: **LRESULT**</span></span>

<span data-ttu-id="483cd-114">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="483cd-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="483cd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="483cd-115">Remarks</span></span>

<span data-ttu-id="483cd-116">Os parâmetros são fornecidos em coordenadas de tela para janelas sobrepostas e pop-up e em coordenadas de cliente pai para janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="483cd-116">The parameters are given in screen coordinates for overlapped and pop-up windows and in parent-client coordinates for child windows.</span></span>

<span data-ttu-id="483cd-117">O exemplo a seguir demonstra como obter a posição do parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="483cd-117">The following example demonstrates how to obtain the position from the *lParam* parameter.</span></span>


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



<span data-ttu-id="483cd-118">Você também pode usar a macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) para converter o parâmetro *lParam* em uma estrutura [**Points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="483cd-118">You can also use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro to convert the *lParam* parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="483cd-119">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia o **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** quando processa a mensagem do [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="483cd-119">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="483cd-120">O **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** não serão enviadas se um aplicativo manipular a mensagem do **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="483cd-120">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="483cd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="483cd-121">Requirements</span></span>



| <span data-ttu-id="483cd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="483cd-122">Requirement</span></span> | <span data-ttu-id="483cd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="483cd-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="483cd-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="483cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="483cd-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="483cd-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="483cd-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="483cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="483cd-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="483cd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="483cd-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="483cd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="483cd-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="483cd-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="483cd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="483cd-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="483cd-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="483cd-131">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="483cd-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="483cd-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="483cd-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="483cd-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="483cd-134">**WINDOWPOSCHANGED do WM \_**</span><span class="sxs-lookup"><span data-stu-id="483cd-134">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="483cd-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="483cd-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="483cd-136">Windows</span><span class="sxs-lookup"><span data-stu-id="483cd-136">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="483cd-137">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="483cd-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="483cd-138">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="483cd-138">**MAKEPOINTS**</span></span>](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="483cd-139">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="483cd-139">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

 
