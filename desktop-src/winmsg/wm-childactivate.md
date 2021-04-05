---
description: Enviado a uma janela filho quando o usuário clica na barra de título da janela ou quando a janela é ativada, movida ou dimensionada.
ms.assetid: 6e60725d-aa01-48bb-86a5-f17f56b97d35
title: Mensagem de WM_CHILDACTIVATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82564a63cfbbbfe5e3693e331c8e990fa934e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662598"
---
# <a name="wm_childactivate-message"></a><span data-ttu-id="b382a-103">Mensagem do WM \_ CHILDACTIVATE</span><span class="sxs-lookup"><span data-stu-id="b382a-103">WM\_CHILDACTIVATE message</span></span>

<span data-ttu-id="b382a-104">Enviado a uma janela filho quando o usuário clica na barra de título da janela ou quando a janela é ativada, movida ou dimensionada.</span><span class="sxs-lookup"><span data-stu-id="b382a-104">Sent to a child window when the user clicks the window's title bar or when the window is activated, moved, or sized.</span></span>

<span data-ttu-id="b382a-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b382a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHILDACTIVATE                0x0022
```



## <a name="parameters"></a><span data-ttu-id="b382a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b382a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b382a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b382a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b382a-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="b382a-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b382a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b382a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b382a-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="b382a-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b382a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b382a-111">Return value</span></span>

<span data-ttu-id="b382a-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b382a-112">Type: **LRESULT**</span></span>

<span data-ttu-id="b382a-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="b382a-113">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b382a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b382a-114">Requirements</span></span>



| <span data-ttu-id="b382a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b382a-115">Requirement</span></span> | <span data-ttu-id="b382a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b382a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b382a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b382a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b382a-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b382a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b382a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b382a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b382a-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b382a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b382a-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b382a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b382a-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b382a-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b382a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b382a-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="b382a-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b382a-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b382a-125">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="b382a-125">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="b382a-126">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="b382a-126">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

<span data-ttu-id="b382a-127">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b382a-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b382a-128">Windows</span><span class="sxs-lookup"><span data-stu-id="b382a-128">Windows</span></span>](windows.md)
</dt> </dl>

 

 
