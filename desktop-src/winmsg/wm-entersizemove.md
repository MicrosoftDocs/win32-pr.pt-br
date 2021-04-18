---
description: Enviado uma vez a uma janela depois de entrar no loop modal de dimensionamento ou movimentação.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Mensagem de WM_ENTERSIZEMOVE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771472"
---
# <a name="wm_entersizemove-message"></a><span data-ttu-id="c68de-103">Mensagem do WM \_ ENTERSIZEMOVE</span><span class="sxs-lookup"><span data-stu-id="c68de-103">WM\_ENTERSIZEMOVE message</span></span>

<span data-ttu-id="c68de-104">Enviado uma vez a uma janela depois de entrar no loop modal de dimensionamento ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="c68de-104">Sent one time to a window after it enters the moving or sizing modal loop.</span></span> <span data-ttu-id="c68de-105">A janela entra no loop modal de dimensionamento ou movimentação quando o usuário clica na barra de título ou na borda de dimensionamento da janela ou quando a janela passa a mensagem [**\_ SYSCOMMAND do WM**](../menurc/wm-syscommand.md) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e o parâmetro *wParam* da mensagem Especifica o valor de **\_ tamanho** **sc \_ move** ou SC.</span><span class="sxs-lookup"><span data-stu-id="c68de-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOVE** or **SC\_SIZE** value.</span></span> <span data-ttu-id="c68de-106">A operação é concluída quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna.</span><span class="sxs-lookup"><span data-stu-id="c68de-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="c68de-107">O sistema envia a mensagem do **WM \_ ENTERSIZEMOVE** , independentemente de o arrasto de janelas completas estar habilitado.</span><span class="sxs-lookup"><span data-stu-id="c68de-107">The system sends the **WM\_ENTERSIZEMOVE** message regardless of whether the dragging of full windows is enabled.</span></span>

<span data-ttu-id="c68de-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c68de-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENTERSIZEMOVE                0x0231
```



## <a name="parameters"></a><span data-ttu-id="c68de-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c68de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c68de-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c68de-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c68de-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="c68de-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c68de-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c68de-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c68de-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="c68de-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c68de-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c68de-114">Return value</span></span>

<span data-ttu-id="c68de-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c68de-115">Type: **LRESULT**</span></span>

<span data-ttu-id="c68de-116">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c68de-116">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c68de-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c68de-117">Requirements</span></span>



| <span data-ttu-id="c68de-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c68de-118">Requirement</span></span> | <span data-ttu-id="c68de-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c68de-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c68de-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c68de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c68de-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c68de-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c68de-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c68de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c68de-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c68de-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c68de-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c68de-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c68de-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c68de-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68de-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c68de-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="c68de-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c68de-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c68de-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c68de-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c68de-129">**EXITSIZEMOVE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c68de-129">**WM\_EXITSIZEMOVE**</span></span>](wm-exitsizemove.md)
</dt> <dt>

[<span data-ttu-id="c68de-130">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c68de-130">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)
</dt> <dt>

<span data-ttu-id="c68de-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c68de-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c68de-132">Windows</span><span class="sxs-lookup"><span data-stu-id="c68de-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
