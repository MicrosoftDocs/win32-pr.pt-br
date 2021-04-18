---
description: Enviado quando um aplicativo solicita que uma janela seja criada chamando a função CreateWindowEx ou CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Mensagem de WM_CREATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786214"
---
# <a name="wm_create-message"></a><span data-ttu-id="6f64d-103">\_Criar mensagem do WM</span><span class="sxs-lookup"><span data-stu-id="6f64d-103">WM\_CREATE message</span></span>

<span data-ttu-id="6f64d-104">Enviado quando um aplicativo solicita que uma janela seja criada chamando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="6f64d-104">Sent when an application requests that a window be created by calling the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="6f64d-105">(A mensagem é enviada antes da função retornar.) O procedimento de janela da nova janela recebe essa mensagem depois que a janela é criada, mas antes de a janela ficar visível.</span><span class="sxs-lookup"><span data-stu-id="6f64d-105">(The message is sent before the function returns.) The window procedure of the new window receives this message after the window is created, but before the window becomes visible.</span></span>

<span data-ttu-id="6f64d-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6f64d-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a><span data-ttu-id="6f64d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f64d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f64d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f64d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f64d-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6f64d-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6f64d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f64d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f64d-111">Um ponteiro para uma estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contém informações sobre a janela que está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="6f64d-111">A pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure that contains information about the window being created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f64d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f64d-112">Return value</span></span>

<span data-ttu-id="6f64d-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f64d-113">Type: **LRESULT**</span></span>

<span data-ttu-id="6f64d-114">Se um aplicativo processar essa mensagem, ele deverá retornar zero para continuar a criação da janela.</span><span class="sxs-lookup"><span data-stu-id="6f64d-114">If an application processes this message, it should return zero to continue creation of the window.</span></span> <span data-ttu-id="6f64d-115">Se o aplicativo retornar – 1, a janela será destruída e a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) retornará um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6f64d-115">If the application returns –1, the window is destroyed and the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) or [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function returns a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f64d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f64d-116">Requirements</span></span>



| <span data-ttu-id="6f64d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f64d-117">Requirement</span></span> | <span data-ttu-id="6f64d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6f64d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f64d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f64d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6f64d-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f64d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6f64d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f64d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6f64d-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f64d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6f64d-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f64d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f64d-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f64d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f64d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f64d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f64d-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6f64d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f64d-127">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="6f64d-127">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="6f64d-128">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="6f64d-128">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="6f64d-129">**OS CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="6f64d-129">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="6f64d-130">**NCCREATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6f64d-130">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="6f64d-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6f64d-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6f64d-132">Windows</span><span class="sxs-lookup"><span data-stu-id="6f64d-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
