---
title: Mensagem de WM_INITMENU (WinUser. h)
description: Enviado quando um menu está prestes a ficar ativo.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764182"
---
# <a name="wm_initmenu-message"></a><span data-ttu-id="c7df9-104">Mensagem do WM \_ INITMENU</span><span class="sxs-lookup"><span data-stu-id="c7df9-104">WM\_INITMENU message</span></span>

<span data-ttu-id="c7df9-105">Enviado quando um menu está prestes a ficar ativo.</span><span class="sxs-lookup"><span data-stu-id="c7df9-105">Sent when a menu is about to become active.</span></span> <span data-ttu-id="c7df9-106">Ele ocorre quando o usuário clica em um item na barra de menus ou pressiona uma tecla de menu.</span><span class="sxs-lookup"><span data-stu-id="c7df9-106">It occurs when the user clicks an item on the menu bar or presses a menu key.</span></span> <span data-ttu-id="c7df9-107">Isso permite que o aplicativo modifique o menu antes que ele seja exibido.</span><span class="sxs-lookup"><span data-stu-id="c7df9-107">This allows the application to modify the menu before it is displayed.</span></span>

<span data-ttu-id="c7df9-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c7df9-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a><span data-ttu-id="c7df9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7df9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7df9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7df9-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7df9-111">Um identificador para o menu a ser inicializado.</span><span class="sxs-lookup"><span data-stu-id="c7df9-111">A handle to the menu to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="c7df9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7df9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7df9-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="c7df9-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7df9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7df9-114">Return value</span></span>

<span data-ttu-id="c7df9-115">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="c7df9-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7df9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7df9-116">Remarks</span></span>

<span data-ttu-id="c7df9-117">Uma mensagem do **WM \_ INITMENU** é enviada somente quando um menu é acessado pela primeira vez; apenas uma mensagem do **WM \_ INITMENU** é gerada para cada acesso.</span><span class="sxs-lookup"><span data-stu-id="c7df9-117">A **WM\_INITMENU** message is sent only when a menu is first accessed; only one **WM\_INITMENU** message is generated for each access.</span></span> <span data-ttu-id="c7df9-118">Por exemplo, mover o mouse em vários itens de menu enquanto mantém pressionado o botão não gera novas mensagens.</span><span class="sxs-lookup"><span data-stu-id="c7df9-118">For example, moving the mouse across several menu items while holding down the button does not generate new messages.</span></span> <span data-ttu-id="c7df9-119">**WM \_ INITMENU** não fornece informações sobre itens de menu.</span><span class="sxs-lookup"><span data-stu-id="c7df9-119">**WM\_INITMENU** does not provide information about menu items.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7df9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7df9-120">Requirements</span></span>



| <span data-ttu-id="c7df9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7df9-121">Requirement</span></span> | <span data-ttu-id="c7df9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c7df9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7df9-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7df9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7df9-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7df9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c7df9-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7df9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7df9-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7df9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7df9-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7df9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7df9-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7df9-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7df9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7df9-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7df9-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c7df9-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7df9-131">**INITMENUPOPUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c7df9-131">**WM\_INITMENUPOPUP**</span></span>](wm-initmenupopup.md)
</dt> <dt>

<span data-ttu-id="c7df9-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c7df9-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7df9-133">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="c7df9-133">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

