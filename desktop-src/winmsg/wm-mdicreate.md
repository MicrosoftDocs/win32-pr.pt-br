---
description: Um aplicativo envia a mensagem do WM \_ MDICREATE para uma janela de cliente MDI (interface de vários documentos) para criar uma janela filho MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Mensagem de WM_MDICREATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793697"
---
# <a name="wm_mdicreate-message"></a><span data-ttu-id="5fc93-103">Mensagem do WM \_ MDICREATE</span><span class="sxs-lookup"><span data-stu-id="5fc93-103">WM\_MDICREATE message</span></span>

<span data-ttu-id="5fc93-104">Um aplicativo envia a mensagem do **WM \_ MDICREATE** para uma janela de cliente MDI (interface de vários documentos) para criar uma janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="5fc93-104">An application sends the **WM\_MDICREATE** message to a multiple-document interface (MDI) client window to create an MDI child window.</span></span>


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a><span data-ttu-id="5fc93-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fc93-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fc93-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5fc93-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc93-107">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="5fc93-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5fc93-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fc93-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fc93-109">Um ponteiro para uma estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) que contém informações que o sistema usa para criar a janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="5fc93-109">A pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure containing information that the system uses to create the MDI child window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fc93-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fc93-110">Return value</span></span>

<span data-ttu-id="5fc93-111">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="5fc93-111">Type: **HWND**</span></span>

<span data-ttu-id="5fc93-112">Se a mensagem tiver sucesso, o valor de retorno será o identificador para a nova janela filho.</span><span class="sxs-lookup"><span data-stu-id="5fc93-112">If the message succeeds, the return value is the handle to the new child window.</span></span>

<span data-ttu-id="5fc93-113">Se a mensagem falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5fc93-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc93-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fc93-114">Remarks</span></span>

<span data-ttu-id="5fc93-115">A janela filho MDI é criada com os bits de [**estilo de janela**](window-styles.md) **WS \_ filho**, **WS \_ CLIPSIBLINGS**, **WS \_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ Caption**, **WS \_ THICKFRAME**, **WS \_ MINIMIZEBOX** e **WS \_ MAXIMIZEBOX**, além de bits de estilo adicionais especificados na estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) .</span><span class="sxs-lookup"><span data-stu-id="5fc93-115">The MDI child window is created with the [**window style**](window-styles.md) bits **WS\_CHILD**, **WS\_CLIPSIBLINGS**, **WS\_CLIPCHILDREN**, **WS\_SYSMENU**, **WS\_CAPTION**, **WS\_THICKFRAME**, **WS\_MINIMIZEBOX**, and **WS\_MAXIMIZEBOX**, plus additional style bits specified in the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="5fc93-116">O sistema adiciona o título da nova janela filho ao menu janela da janela do quadro.</span><span class="sxs-lookup"><span data-stu-id="5fc93-116">The system adds the title of the new child window to the window menu of the frame window.</span></span> <span data-ttu-id="5fc93-117">Um aplicativo deve usar essa mensagem para criar todas as janelas filhas da janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="5fc93-117">An application should use this message to create all child windows of the client window.</span></span>

<span data-ttu-id="5fc93-118">Se uma janela do cliente MDI receber qualquer mensagem que altere a ativação de suas janelas filhas enquanto a janela filho ativa for maximizada, o sistema restaura a janela filho ativa e maximiza a janela filho ativada recentemente.</span><span class="sxs-lookup"><span data-stu-id="5fc93-118">If an MDI client window receives any message that changes the activation of its child windows while the active child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

<span data-ttu-id="5fc93-119">Quando uma janela filho MDI é criada, o sistema envia a mensagem de [**\_ criação do WM**](wm-create.md) para a janela.</span><span class="sxs-lookup"><span data-stu-id="5fc93-119">When an MDI child window is created, the system sends the [**WM\_CREATE**](wm-create.md) message to the window.</span></span> <span data-ttu-id="5fc93-120">O parâmetro *lParam* da mensagem **de \_ criação do WM** contém um ponteiro para uma estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) .</span><span class="sxs-lookup"><span data-stu-id="5fc93-120">The *lParam* parameter of the **WM\_CREATE** message contains a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="5fc93-121">O membro *lpCreateParams* dessa estrutura contém um ponteiro para a estrutura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) passada com a mensagem **\_ MDICREATE do WM** que criou a janela filho MDI.</span><span class="sxs-lookup"><span data-stu-id="5fc93-121">The *lpCreateParams* member of this structure contains a pointer to the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure passed with the **WM\_MDICREATE** message that created the MDI child window.</span></span>

<span data-ttu-id="5fc93-122">Um aplicativo não deve enviar uma segunda mensagem do **WM \_ MDICREATE** enquanto uma mensagem do **WM \_ MDICREATE** ainda está sendo processada.</span><span class="sxs-lookup"><span data-stu-id="5fc93-122">An application should not send a second **WM\_MDICREATE** message while a **WM\_MDICREATE** message is still being processed.</span></span> <span data-ttu-id="5fc93-123">Por exemplo, ele não deve enviar uma mensagem do **WM \_ MDICREATE** enquanto uma janela filho MDI processa sua mensagem do **WM \_ MDICREATE** .</span><span class="sxs-lookup"><span data-stu-id="5fc93-123">For example, it should not send a **WM\_MDICREATE** message while an MDI child window is processing its **WM\_MDICREATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fc93-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fc93-124">Requirements</span></span>



| <span data-ttu-id="5fc93-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc93-125">Requirement</span></span> | <span data-ttu-id="5fc93-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5fc93-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc93-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fc93-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc93-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5fc93-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5fc93-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fc93-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc93-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5fc93-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5fc93-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5fc93-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fc93-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fc93-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fc93-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fc93-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="5fc93-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5fc93-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5fc93-135">**CreateMDIWindow**</span><span class="sxs-lookup"><span data-stu-id="5fc93-135">**CreateMDIWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[<span data-ttu-id="5fc93-136">**OS CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5fc93-136">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="5fc93-137">**MDICREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5fc93-137">**MDICREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[<span data-ttu-id="5fc93-138">**criação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5fc93-138">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

[<span data-ttu-id="5fc93-139">**MDIDESTROY do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5fc93-139">**WM\_MDIDESTROY**</span></span>](wm-mdidestroy.md)
</dt> <dt>

<span data-ttu-id="5fc93-140">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5fc93-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5fc93-141">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="5fc93-141">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
