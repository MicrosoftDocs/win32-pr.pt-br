---
description: Enviado quando uma janela pertencente a um aplicativo diferente da janela ativa está prestes a ser ativada. A mensagem é enviada ao aplicativo cuja janela está sendo ativada e ao aplicativo cuja janela está sendo desativada.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Mensagem de WM_ACTIVATEAPP (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763033"
---
# <a name="wm_activateapp-message"></a><span data-ttu-id="62b6a-104">Mensagem do WM \_ ACTIVATEAPP</span><span class="sxs-lookup"><span data-stu-id="62b6a-104">WM\_ACTIVATEAPP message</span></span>

<span data-ttu-id="62b6a-105">Enviado quando uma janela pertencente a um aplicativo diferente da janela ativa está prestes a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="62b6a-105">Sent when a window belonging to a different application than the active window is about to be activated.</span></span> <span data-ttu-id="62b6a-106">A mensagem é enviada ao aplicativo cuja janela está sendo ativada e ao aplicativo cuja janela está sendo desativada.</span><span class="sxs-lookup"><span data-stu-id="62b6a-106">The message is sent to the application whose window is being activated and to the application whose window is being deactivated.</span></span>

<span data-ttu-id="62b6a-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="62b6a-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a><span data-ttu-id="62b6a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62b6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62b6a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62b6a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62b6a-110">Indica se a janela está sendo ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="62b6a-110">Indicates whether the window is being activated or deactivated.</span></span> <span data-ttu-id="62b6a-111">Esse parâmetro será **true** se a janela estiver sendo ativada; será **false** se a janela estiver sendo desativada.</span><span class="sxs-lookup"><span data-stu-id="62b6a-111">This parameter is **TRUE** if the window is being activated; it is **FALSE** if the window is being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="62b6a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62b6a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62b6a-113">O identificador de thread.</span><span class="sxs-lookup"><span data-stu-id="62b6a-113">The thread identifier.</span></span> <span data-ttu-id="62b6a-114">Se o parâmetro *wParam* for **true**, *lParam* será o identificador do thread que possui a janela que está sendo desativada.</span><span class="sxs-lookup"><span data-stu-id="62b6a-114">If the *wParam* parameter is **TRUE**, *lParam* is the identifier of the thread that owns the window being deactivated.</span></span> <span data-ttu-id="62b6a-115">Se *wParam* for **false**, *lParam* será o identificador do thread que possui a janela que está sendo ativada.</span><span class="sxs-lookup"><span data-stu-id="62b6a-115">If *wParam* is **FALSE**, *lParam* is the identifier of the thread that owns the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62b6a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62b6a-116">Return value</span></span>

<span data-ttu-id="62b6a-117">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="62b6a-117">Type: **LRESULT**</span></span>

<span data-ttu-id="62b6a-118">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="62b6a-118">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="62b6a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62b6a-119">Requirements</span></span>



| <span data-ttu-id="62b6a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62b6a-120">Requirement</span></span> | <span data-ttu-id="62b6a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="62b6a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b6a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62b6a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62b6a-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="62b6a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="62b6a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62b6a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62b6a-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="62b6a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62b6a-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="62b6a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="62b6a-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62b6a-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b6a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="62b6a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="62b6a-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="62b6a-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62b6a-130">**ativar o WM \_**</span><span class="sxs-lookup"><span data-stu-id="62b6a-130">**WM\_ACTIVATE**</span></span>](../inputdev/wm-activate.md)
</dt> <dt>

<span data-ttu-id="62b6a-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="62b6a-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62b6a-132">Windows</span><span class="sxs-lookup"><span data-stu-id="62b6a-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
