---
description: Transmita para cada janela após um evento de alteração de tema. Exemplos de eventos de alteração de tema são a ativação de um tema, a desativação de um tema ou uma transição de um tema para outro.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: Mensagem de WM_THEMECHANGED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15ab64126ff8972b858ef43ddd4d92cd62f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647074"
---
# <a name="wm_themechanged-message"></a><span data-ttu-id="c1134-104">\_Mensagem themechanged do WM</span><span class="sxs-lookup"><span data-stu-id="c1134-104">WM\_THEMECHANGED message</span></span>

<span data-ttu-id="c1134-105">Transmita para cada janela após um evento de alteração de tema.</span><span class="sxs-lookup"><span data-stu-id="c1134-105">Broadcast to every window following a theme change event.</span></span> <span data-ttu-id="c1134-106">Exemplos de eventos de alteração de tema são a ativação de um tema, a desativação de um tema ou uma transição de um tema para outro.</span><span class="sxs-lookup"><span data-stu-id="c1134-106">Examples of theme change events are the activation of a theme, the deactivation of a theme, or a transition from one theme to another.</span></span>


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a><span data-ttu-id="c1134-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1134-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1134-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1134-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1134-109">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="c1134-109">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c1134-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1134-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1134-111">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="c1134-111">This parameter is reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1134-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1134-112">Return value</span></span>

<span data-ttu-id="c1134-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c1134-113">Type: **LRESULT**</span></span>

<span data-ttu-id="c1134-114">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="c1134-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1134-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1134-115">Remarks</span></span>

<span data-ttu-id="c1134-116">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c1134-116">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="c1134-117">Essa mensagem é postada pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c1134-117">This message is posted by the operating system.</span></span> <span data-ttu-id="c1134-118">Normalmente, os aplicativos não enviam essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c1134-118">Applications typically do not send this message.</span></span>

 

<span data-ttu-id="c1134-119">Os temas são especificações para a aparência de controles, para que o elemento visual de um controle seja tratado separadamente de sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="c1134-119">Themes are specifications for the appearance of controls, so that the visual element of a control is treated separately from its functionality.</span></span>

<span data-ttu-id="c1134-120">Para liberar um identificador de tema existente, chame [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span><span class="sxs-lookup"><span data-stu-id="c1134-120">To release an existing theme handle, call [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata).</span></span> <span data-ttu-id="c1134-121">Para adquirir um novo identificador de tema, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span><span class="sxs-lookup"><span data-stu-id="c1134-121">To acquire a new theme handle, use [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).</span></span>

<span data-ttu-id="c1134-122">Seguindo a **transmissão \_ themechanged do WM** , quaisquer identificadores de tema existentes são inválidos.</span><span class="sxs-lookup"><span data-stu-id="c1134-122">Following the **WM\_THEMECHANGED** broadcast, any existing theme handles are invalid.</span></span> <span data-ttu-id="c1134-123">Uma janela com reconhecimento de tema deve liberar e reabrir qualquer uma de suas alças de tema preexistentes quando recebe a mensagem **\_ themechanged do WM** .</span><span class="sxs-lookup"><span data-stu-id="c1134-123">A theme-aware window should release and reopen any of its pre-existing theme handles when it receives the **WM\_THEMECHANGED** message.</span></span> <span data-ttu-id="c1134-124">Se a função [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) retornar **NULL**, a janela deverá ser despintada.</span><span class="sxs-lookup"><span data-stu-id="c1134-124">If the [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) function returns **NULL**, the window should paint unthemed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1134-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1134-125">Requirements</span></span>



| <span data-ttu-id="c1134-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1134-126">Requirement</span></span> | <span data-ttu-id="c1134-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c1134-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1134-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1134-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c1134-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c1134-129">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1134-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1134-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c1134-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1134-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1134-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1134-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1134-133"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1134-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1134-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1134-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1134-135">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="c1134-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c1134-136">**CloseThemeData**</span><span class="sxs-lookup"><span data-stu-id="c1134-136">**CloseThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[<span data-ttu-id="c1134-137">**IsThemeActive**</span><span class="sxs-lookup"><span data-stu-id="c1134-137">**IsThemeActive**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[<span data-ttu-id="c1134-138">**OpenThemeData**</span><span class="sxs-lookup"><span data-stu-id="c1134-138">**OpenThemeData**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
