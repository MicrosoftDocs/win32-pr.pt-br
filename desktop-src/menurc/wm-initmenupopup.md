---
title: Mensagem de WM_INITMENUPOPUP (WinUser. h)
description: WM_INITMENUPOPUP mensagem enviada quando um menu suspenso ou submenu está prestes a ficar ativo. Isso permite que um aplicativo modifique o menu antes que ele seja exibido, sem alterar o menu inteiro.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d850547d57596dd36b36b941d1782c2aee1f5b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092514"
---
# <a name="wm_initmenupopup-message"></a><span data-ttu-id="9fa74-105">Mensagem do WM \_ INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="9fa74-105">WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="9fa74-106">Enviado quando um menu suspenso ou submenu está prestes a ficar ativo.</span><span class="sxs-lookup"><span data-stu-id="9fa74-106">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="9fa74-107">Isso permite que um aplicativo modifique o menu antes que ele seja exibido, sem alterar o menu inteiro.</span><span class="sxs-lookup"><span data-stu-id="9fa74-107">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a><span data-ttu-id="9fa74-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fa74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fa74-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fa74-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fa74-110">Um identificador para o menu suspenso ou submenu.</span><span class="sxs-lookup"><span data-stu-id="9fa74-110">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="9fa74-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fa74-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fa74-112">A palavra de ordem inferior Especifica a posição relativa de base zero do item de menu que abre o menu suspenso ou o submenu.</span><span class="sxs-lookup"><span data-stu-id="9fa74-112">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="9fa74-113">A palavra de ordem superior indica se o menu suspenso é o menu janela.</span><span class="sxs-lookup"><span data-stu-id="9fa74-113">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="9fa74-114">Se o menu for o menu janela, esse parâmetro será **true**; caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="9fa74-114">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fa74-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9fa74-115">Return value</span></span>

<span data-ttu-id="9fa74-116">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="9fa74-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa74-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fa74-117">Requirements</span></span>



| <span data-ttu-id="9fa74-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fa74-118">Requirement</span></span> | <span data-ttu-id="9fa74-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9fa74-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa74-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fa74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa74-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9fa74-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9fa74-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fa74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa74-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9fa74-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9fa74-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9fa74-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fa74-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fa74-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fa74-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9fa74-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9fa74-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9fa74-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="9fa74-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fa74-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9fa74-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fa74-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9fa74-130">**INITMENU do WM \_**</span><span class="sxs-lookup"><span data-stu-id="9fa74-130">**WM\_INITMENU**</span></span>](wm-initmenu.md)
</dt> <dt>

<span data-ttu-id="9fa74-131">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="9fa74-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9fa74-132">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="9fa74-132">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

