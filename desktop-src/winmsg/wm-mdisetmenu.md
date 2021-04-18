---
description: Um aplicativo envia a mensagem do WM \_ MDISETMENU para uma janela de cliente MDI (interface de vários documentos) para substituir o menu inteiro de uma janela de quadro MDI, para substituir o menu janela da janela do quadro ou ambos.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Mensagem de WM_MDISETMENU (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793720"
---
# <a name="wm_mdisetmenu-message"></a><span data-ttu-id="c2126-103">Mensagem do WM \_ MDISETMENU</span><span class="sxs-lookup"><span data-stu-id="c2126-103">WM\_MDISETMENU message</span></span>

<span data-ttu-id="c2126-104">Um aplicativo envia a mensagem do **WM \_ MDISETMENU** para uma janela de cliente MDI (interface de vários documentos) para substituir o menu inteiro de uma janela de quadro MDI, para substituir o menu janela da janela do quadro ou ambos.</span><span class="sxs-lookup"><span data-stu-id="c2126-104">An application sends the **WM\_MDISETMENU** message to a multiple-document interface (MDI) client window to replace the entire menu of an MDI frame window, to replace the window menu of the frame window, or both.</span></span>


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a><span data-ttu-id="c2126-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2126-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2126-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2126-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2126-107">Um identificador para o novo menu da janela de quadros.</span><span class="sxs-lookup"><span data-stu-id="c2126-107">A handle to the new frame window menu.</span></span> <span data-ttu-id="c2126-108">Se esse parâmetro for **nulo**, o menu janela do quadro não será alterado.</span><span class="sxs-lookup"><span data-stu-id="c2126-108">If this parameter is **NULL**, the frame window menu is not changed.</span></span>

</dd> <dt>

<span data-ttu-id="c2126-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2126-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2126-110">Um identificador para o novo menu de janela.</span><span class="sxs-lookup"><span data-stu-id="c2126-110">A handle to the new window menu.</span></span> <span data-ttu-id="c2126-111">Se esse parâmetro for **nulo**, o menu janela não será alterado.</span><span class="sxs-lookup"><span data-stu-id="c2126-111">If this parameter is **NULL**, the window menu is not changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2126-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2126-112">Return value</span></span>

<span data-ttu-id="c2126-113">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="c2126-113">Type: **HMENU**</span></span>

<span data-ttu-id="c2126-114">Se a mensagem tiver sucesso, o valor de retorno será o identificador para o menu da janela do quadro antigo.</span><span class="sxs-lookup"><span data-stu-id="c2126-114">If the message succeeds, the return value is the handle to the old frame window menu.</span></span>

<span data-ttu-id="c2126-115">Se a mensagem falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="c2126-115">If the message fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2126-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2126-116">Remarks</span></span>

<span data-ttu-id="c2126-117">Depois de enviar essa mensagem, um aplicativo deve chamar a função [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para atualizar a barra de menus.</span><span class="sxs-lookup"><span data-stu-id="c2126-117">After sending this message, an application must call the [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) function to update the menu bar.</span></span>

<span data-ttu-id="c2126-118">Se essa mensagem substituir o menu janela, os itens de menu da janela filho MDI serão removidos do menu da janela anterior e adicionados ao menu nova janela.</span><span class="sxs-lookup"><span data-stu-id="c2126-118">If this message replaces the window menu, the MDI child window menu items are removed from the previous window menu and added to the new window menu.</span></span>

<span data-ttu-id="c2126-119">Se uma janela filho MDI for maximizada e essa mensagem substituir o menu de janela do quadro MDI, o ícone do menu janela e o ícone restaurar serão removidos do menu da janela do quadro anterior e adicionados ao menu nova janela do quadro.</span><span class="sxs-lookup"><span data-stu-id="c2126-119">If an MDI child window is maximized and this message replaces the MDI frame window menu, the window menu icon and restore icon are removed from the previous frame window menu and added to the new frame window menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2126-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2126-120">Requirements</span></span>



| <span data-ttu-id="c2126-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2126-121">Requirement</span></span> | <span data-ttu-id="c2126-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c2126-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2126-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2126-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c2126-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2126-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c2126-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2126-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c2126-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2126-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c2126-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2126-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2126-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2126-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2126-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2126-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c2126-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c2126-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c2126-131">**DrawMenuBar**</span><span class="sxs-lookup"><span data-stu-id="c2126-131">**DrawMenuBar**</span></span>](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[<span data-ttu-id="c2126-132">**MDIREFRESHMENU do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c2126-132">**WM\_MDIREFRESHMENU**</span></span>](wm-mdirefreshmenu.md)
</dt> <dt>

<span data-ttu-id="c2126-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c2126-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c2126-134">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="c2126-134">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
