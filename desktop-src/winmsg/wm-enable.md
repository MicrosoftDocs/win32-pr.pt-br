---
description: Enviado quando um aplicativo altera o estado habilitado de uma janela.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Mensagem de WM_ENABLE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783722"
---
# <a name="wm_enable-message"></a><span data-ttu-id="7010c-103">\_Mensagem de habilitação do WM</span><span class="sxs-lookup"><span data-stu-id="7010c-103">WM\_ENABLE message</span></span>

<span data-ttu-id="7010c-104">Enviado quando um aplicativo altera o estado habilitado de uma janela.</span><span class="sxs-lookup"><span data-stu-id="7010c-104">Sent when an application changes the enabled state of a window.</span></span> <span data-ttu-id="7010c-105">Ele é enviado para a janela cujo estado habilitado está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="7010c-105">It is sent to the window whose enabled state is changing.</span></span> <span data-ttu-id="7010c-106">Essa mensagem é enviada antes que a função [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) retorne, mas após o estado habilitado (o bit WS-State do estilo) da janela foi alterado.[**\_**](window-styles.md)</span><span class="sxs-lookup"><span data-stu-id="7010c-106">This message is sent before the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function returns, but after the enabled state ([**WS\_DISABLED**](window-styles.md) style bit) of the window has changed.</span></span>

<span data-ttu-id="7010c-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7010c-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a><span data-ttu-id="7010c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7010c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7010c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7010c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7010c-110">Indica se a janela foi habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7010c-110">Indicates whether the window has been enabled or disabled.</span></span> <span data-ttu-id="7010c-111">Esse parâmetro será **true** se a janela tiver sido habilitada ou **falsa** se a janela tiver sido desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7010c-111">This parameter is **TRUE** if the window has been enabled or **FALSE** if the window has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="7010c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7010c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7010c-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="7010c-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7010c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7010c-114">Return value</span></span>

<span data-ttu-id="7010c-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7010c-115">Type: **LRESULT**</span></span>

<span data-ttu-id="7010c-116">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="7010c-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7010c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7010c-117">Requirements</span></span>



| <span data-ttu-id="7010c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7010c-118">Requirement</span></span> | <span data-ttu-id="7010c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7010c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7010c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7010c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7010c-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7010c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7010c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7010c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7010c-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7010c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7010c-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7010c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7010c-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7010c-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7010c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7010c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7010c-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7010c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7010c-128">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="7010c-128">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

<span data-ttu-id="7010c-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7010c-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7010c-130">Windows</span><span class="sxs-lookup"><span data-stu-id="7010c-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
