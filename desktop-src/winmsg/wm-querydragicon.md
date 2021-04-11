---
description: Enviado para uma janela minimizada (icônico).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Mensagem de WM_QUERYDRAGICON (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296765"
---
# <a name="wm_querydragicon-message"></a><span data-ttu-id="74654-103">Mensagem do WM \_ QUERYDRAGICON</span><span class="sxs-lookup"><span data-stu-id="74654-103">WM\_QUERYDRAGICON message</span></span>

<span data-ttu-id="74654-104">Enviado para uma janela minimizada (icônico).</span><span class="sxs-lookup"><span data-stu-id="74654-104">Sent to a minimized (iconic) window.</span></span> <span data-ttu-id="74654-105">A janela está prestes a ser arrastada pelo usuário, mas não tem um ícone definido para sua classe.</span><span class="sxs-lookup"><span data-stu-id="74654-105">The window is about to be dragged by the user but does not have an icon defined for its class.</span></span> <span data-ttu-id="74654-106">Um aplicativo pode retornar um identificador para um ícone ou cursor.</span><span class="sxs-lookup"><span data-stu-id="74654-106">An application can return a handle to an icon or cursor.</span></span> <span data-ttu-id="74654-107">O sistema exibe esse cursor ou ícone enquanto o usuário arrasta o ícone.</span><span class="sxs-lookup"><span data-stu-id="74654-107">The system displays this cursor or icon while the user drags the icon.</span></span>

<span data-ttu-id="74654-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="74654-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a><span data-ttu-id="74654-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74654-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74654-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74654-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74654-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="74654-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="74654-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74654-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74654-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="74654-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74654-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74654-114">Return value</span></span>

<span data-ttu-id="74654-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="74654-115">Type: **LRESULT**</span></span>

<span data-ttu-id="74654-116">Um aplicativo deve retornar um identificador para um cursor ou um ícone que o sistema deverá exibir enquanto o usuário arrasta o ícone.</span><span class="sxs-lookup"><span data-stu-id="74654-116">An application should return a handle to a cursor or icon that the system is to display while the user drags the icon.</span></span> <span data-ttu-id="74654-117">O cursor ou o ícone deve ser compatível com a resolução do driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="74654-117">The cursor or icon must be compatible with the display driver's resolution.</span></span> <span data-ttu-id="74654-118">Se o aplicativo retornar **nulo**, o sistema exibirá o cursor padrão.</span><span class="sxs-lookup"><span data-stu-id="74654-118">If the application returns **NULL**, the system displays the default cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="74654-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="74654-119">Remarks</span></span>

<span data-ttu-id="74654-120">Quando o usuário arrasta o ícone de uma janela sem um ícone de classe, o sistema substitui o ícone por um cursor padrão.</span><span class="sxs-lookup"><span data-stu-id="74654-120">When the user drags the icon of a window without a class icon, the system replaces the icon with a default cursor.</span></span> <span data-ttu-id="74654-121">Se o aplicativo exigir que um cursor diferente seja exibido durante a arrastar, ele deverá retornar um identificador para o cursor ou ícone compatível com a resolução do driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="74654-121">If the application requires a different cursor to be displayed during dragging, it must return a handle to the cursor or icon compatible with the display driver's resolution.</span></span> <span data-ttu-id="74654-122">Se um aplicativo retornar um identificador para um cursor ou ícone de cor, o sistema converterá o cursor ou o ícone em preto e branco.</span><span class="sxs-lookup"><span data-stu-id="74654-122">If an application returns a handle to a color cursor or icon, the system converts the cursor or icon to black and white.</span></span> <span data-ttu-id="74654-123">O aplicativo pode chamar a função [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) ou [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para carregar um cursor ou um ícone dos recursos em seu arquivo executável (. exe) e recuperar esse identificador.</span><span class="sxs-lookup"><span data-stu-id="74654-123">The application can call the [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) or [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to load a cursor or icon from the resources in its executable (.exe) file and to retrieve this handle.</span></span>

<span data-ttu-id="74654-124">Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um **bool** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="74654-124">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="74654-125">O valor de **\_ MSGRESULT DWL** definido pela função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="74654-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="74654-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74654-126">Requirements</span></span>



| <span data-ttu-id="74654-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="74654-127">Requirement</span></span> | <span data-ttu-id="74654-128">Valor</span><span class="sxs-lookup"><span data-stu-id="74654-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74654-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74654-129">Minimum supported client</span></span><br/> | <span data-ttu-id="74654-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="74654-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="74654-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74654-131">Minimum supported server</span></span><br/> | <span data-ttu-id="74654-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="74654-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="74654-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="74654-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="74654-134"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74654-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74654-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="74654-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="74654-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="74654-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="74654-137">**LoadCursor**</span><span class="sxs-lookup"><span data-stu-id="74654-137">**LoadCursor**</span></span>](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[<span data-ttu-id="74654-138">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="74654-138">**LoadIcon**</span></span>](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

<span data-ttu-id="74654-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="74654-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="74654-140">Windows</span><span class="sxs-lookup"><span data-stu-id="74654-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
