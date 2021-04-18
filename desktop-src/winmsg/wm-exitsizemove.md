---
description: Enviado uma vez a uma janela, depois de sair do loop modal de dimensionamento ou movimentação.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Mensagem de WM_EXITSIZEMOVE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788782"
---
# <a name="wm_exitsizemove-message"></a><span data-ttu-id="9ce1c-103">Mensagem do WM \_ EXITSIZEMOVE</span><span class="sxs-lookup"><span data-stu-id="9ce1c-103">WM\_EXITSIZEMOVE message</span></span>

<span data-ttu-id="9ce1c-104">Enviado uma vez a uma janela, depois de sair do loop modal de dimensionamento ou movimentação.</span><span class="sxs-lookup"><span data-stu-id="9ce1c-104">Sent one time to a window, after it has exited the moving or sizing modal loop.</span></span> <span data-ttu-id="9ce1c-105">A janela entra no loop modal de dimensionamento ou movimentação quando o usuário clica na barra de título ou na borda de dimensionamento da janela ou quando a janela passa a mensagem [**\_ SYSCOMMAND do WM**](../menurc/wm-syscommand.md) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e o parâmetro *wParam* da mensagem Especifica o valor de **\_ tamanho** **sc \_ Mov** E ou SC.</span><span class="sxs-lookup"><span data-stu-id="9ce1c-105">The window enters the moving or sizing modal loop when the user clicks the window's title bar or sizing border, or when the window passes the [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function and the *wParam* parameter of the message specifies the **SC\_MOV** E or **SC\_SIZE** value.</span></span> <span data-ttu-id="9ce1c-106">A operação é concluída quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna.</span><span class="sxs-lookup"><span data-stu-id="9ce1c-106">The operation is complete when [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns.</span></span>

<span data-ttu-id="9ce1c-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9ce1c-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a><span data-ttu-id="9ce1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ce1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ce1c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ce1c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce1c-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="9ce1c-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9ce1c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ce1c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ce1c-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="9ce1c-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ce1c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ce1c-113">Return value</span></span>

<span data-ttu-id="9ce1c-114">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9ce1c-114">Type: **LRESULT**</span></span>

<span data-ttu-id="9ce1c-115">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ce1c-115">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ce1c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ce1c-116">Requirements</span></span>



| <span data-ttu-id="9ce1c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ce1c-117">Requirement</span></span> | <span data-ttu-id="9ce1c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9ce1c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce1c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ce1c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce1c-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ce1c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9ce1c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ce1c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce1c-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ce1c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ce1c-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9ce1c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ce1c-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ce1c-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce1c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ce1c-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ce1c-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9ce1c-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ce1c-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9ce1c-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9ce1c-128">**ENTERSIZEMOVE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="9ce1c-128">**WM\_ENTERSIZEMOVE**</span></span>](wm-entersizemove.md)
</dt> <dt>

<span data-ttu-id="9ce1c-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="9ce1c-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ce1c-130">Windows</span><span class="sxs-lookup"><span data-stu-id="9ce1c-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
