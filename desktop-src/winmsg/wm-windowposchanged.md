---
description: Enviado a uma janela cujo tamanho, posição ou lugar na ordem Z foi alterado como resultado de uma chamada para a função SetWindowPos ou outra função de gerenciamento de janela.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Mensagem de WM_WINDOWPOSCHANGED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090275"
---
# <a name="wm_windowposchanged-message"></a><span data-ttu-id="d1a5a-103">Mensagem do WM \_ WINDOWPOSCHANGED</span><span class="sxs-lookup"><span data-stu-id="d1a5a-103">WM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="d1a5a-104">Enviado a uma janela cujo tamanho, posição ou lugar na ordem Z foi alterado como resultado de uma chamada para a função [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou outra função de gerenciamento de janela.</span><span class="sxs-lookup"><span data-stu-id="d1a5a-104">Sent to a window whose size, position, or place in the Z order has changed as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="d1a5a-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d1a5a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a><span data-ttu-id="d1a5a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1a5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a5a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1a5a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5a-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="d1a5a-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d1a5a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1a5a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a5a-110">Um ponteiro para uma estrutura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que contém informações sobre o novo tamanho e a posição da janela.</span><span class="sxs-lookup"><span data-stu-id="d1a5a-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a5a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1a5a-111">Return value</span></span>

<span data-ttu-id="d1a5a-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-112">Type: **LRESULT**</span></span>

<span data-ttu-id="d1a5a-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="d1a5a-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1a5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1a5a-114">Remarks</span></span>

<span data-ttu-id="d1a5a-115">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia o [**\_ tamanho do WM**](wm-size.md) e as mensagens de [**\_ movimentação do WM**](wm-move.md) para a janela.</span><span class="sxs-lookup"><span data-stu-id="d1a5a-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_SIZE**](wm-size.md) and [**WM\_MOVE**](wm-move.md) messages to the window.</span></span> <span data-ttu-id="d1a5a-116">O **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** não serão enviadas se um aplicativo manipular a mensagem do **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="d1a5a-116">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span> <span data-ttu-id="d1a5a-117">É mais eficiente executar qualquer processamento de alteração de movimentação ou de tamanho durante a mensagem de **\_ WINDOWPOSCHANGED do WM** sem chamar **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="d1a5a-117">It is more efficient to perform any move or size change processing during the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a5a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1a5a-118">Requirements</span></span>



| <span data-ttu-id="d1a5a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1a5a-119">Requirement</span></span> | <span data-ttu-id="d1a5a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d1a5a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a5a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1a5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a5a-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1a5a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d1a5a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1a5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a5a-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1a5a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1a5a-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d1a5a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1a5a-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1a5a-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a5a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1a5a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1a5a-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1a5a-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d1a5a-130">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-130">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="d1a5a-131">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-131">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="d1a5a-132">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-132">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="d1a5a-133">**movimentação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-133">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="d1a5a-134">**tamanho do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-134">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="d1a5a-135">**WINDOWPOSCHANGING do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-135">**WM\_WINDOWPOSCHANGING**</span></span>](wm-windowposchanging.md)
</dt> <dt>

<span data-ttu-id="d1a5a-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d1a5a-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d1a5a-137">Windows</span><span class="sxs-lookup"><span data-stu-id="d1a5a-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
