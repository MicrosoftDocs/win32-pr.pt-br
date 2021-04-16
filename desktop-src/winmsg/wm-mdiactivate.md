---
description: Um aplicativo envia a mensagem do WM \_ MDIACTIVATE para uma janela de cliente MDI (interface de vários documentos) para instruir a janela do cliente a ativar uma janela filho MDI diferente.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: Mensagem de WM_MDIACTIVATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751346"
---
# <a name="wm_mdiactivate-message"></a><span data-ttu-id="7c629-103">Mensagem do WM \_ MDIACTIVATE</span><span class="sxs-lookup"><span data-stu-id="7c629-103">WM\_MDIACTIVATE message</span></span>

<span data-ttu-id="7c629-104">Um aplicativo envia a mensagem do **WM \_ MDIACTIVATE** para uma janela de cliente MDI (interface de vários documentos) para instruir a janela do cliente a ativar uma janela filho MDI diferente.</span><span class="sxs-lookup"><span data-stu-id="7c629-104">An application sends the **WM\_MDIACTIVATE** message to a multiple-document interface (MDI) client window to instruct the client window to activate a different MDI child window.</span></span>


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a><span data-ttu-id="7c629-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c629-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c629-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c629-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c629-107">Um identificador para a janela filho MDI a ser ativado.</span><span class="sxs-lookup"><span data-stu-id="7c629-107">A handle to the MDI child window to be activated.</span></span>

</dd> <dt>

<span data-ttu-id="7c629-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c629-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c629-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="7c629-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c629-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c629-110">Return value</span></span>

<span data-ttu-id="7c629-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="7c629-111">Type: **LRESULT**</span></span>

<span data-ttu-id="7c629-112">Se um aplicativo enviar essa mensagem para uma janela de cliente do MDI, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="7c629-112">If an application sends this message to an MDI client window, the return value is zero.</span></span>

<span data-ttu-id="7c629-113">Uma janela filho MDI deve retornar zero se ela processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="7c629-113">An MDI child window should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c629-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c629-114">Remarks</span></span>

<span data-ttu-id="7c629-115">À medida que a janela do cliente processa essa mensagem, ela envia o **WM \_ MDIACTIVATE** para a janela filho que está sendo desativada e para a janela filho que está sendo ativada.</span><span class="sxs-lookup"><span data-stu-id="7c629-115">As the client window processes this message, it sends **WM\_MDIACTIVATE** to the child window being deactivated and to the child window being activated.</span></span> <span data-ttu-id="7c629-116">Os parâmetros de mensagem recebidos por uma janela filho MDI são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7c629-116">The message parameters received by an MDI child window are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="7c629-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c629-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="7c629-118">Um identificador para a janela filho MDI que está sendo desativada.</span><span class="sxs-lookup"><span data-stu-id="7c629-118">A handle to the MDI child window being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="7c629-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c629-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="7c629-120">Um identificador para a janela filho MDI que está sendo ativada.</span><span class="sxs-lookup"><span data-stu-id="7c629-120">A handle to the MDI child window being activated.</span></span>

</dd> </dl>

<span data-ttu-id="7c629-121">Uma janela filho MDI é ativada independentemente da janela do quadro MDI.</span><span class="sxs-lookup"><span data-stu-id="7c629-121">An MDI child window is activated independently of the MDI frame window.</span></span> <span data-ttu-id="7c629-122">Quando a janela do quadro se torna ativa, a janela filho ativada pela última vez usando a mensagem do **WM \_ MDIACTIVATE** recebe a mensagem do [**WM \_ NCACTIVATE**](wm-ncactivate.md) para desenhar um quadro de janela ativa e uma barra de título; a janela filho não recebe outra mensagem do **WM \_ MDIACTIVATE** .</span><span class="sxs-lookup"><span data-stu-id="7c629-122">When the frame window becomes active, the child window last activated by using the **WM\_MDIACTIVATE** message receives the [**WM\_NCACTIVATE**](wm-ncactivate.md) message to draw an active window frame and title bar; the child window does not receive another **WM\_MDIACTIVATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c629-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c629-123">Requirements</span></span>



| <span data-ttu-id="7c629-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c629-124">Requirement</span></span> | <span data-ttu-id="7c629-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7c629-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c629-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c629-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7c629-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c629-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7c629-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c629-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7c629-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c629-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7c629-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c629-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c629-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c629-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c629-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c629-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c629-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7c629-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c629-134">**MDIGETACTIVE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7c629-134">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

[<span data-ttu-id="7c629-135">**MDINEXT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7c629-135">**WM\_MDINEXT**</span></span>](wm-mdinext.md)
</dt> <dt>

[<span data-ttu-id="7c629-136">**NCACTIVATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7c629-136">**WM\_NCACTIVATE**</span></span>](wm-ncactivate.md)
</dt> <dt>

<span data-ttu-id="7c629-137">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="7c629-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7c629-138">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="7c629-138">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




