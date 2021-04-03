---
description: Enviado a uma janela quando o tamanho ou a posição da janela está prestes a ser alterada. Um aplicativo pode usar essa mensagem para substituir o tamanho e a posição padrão da janela, ou seu tamanho de rastreamento mínimo ou máximo padrão.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Mensagem de WM_GETMINMAXINFO (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829209"
---
# <a name="wm_getminmaxinfo-message"></a><span data-ttu-id="2c8e6-104">Mensagem do WM \_ GETMINMAXINFO</span><span class="sxs-lookup"><span data-stu-id="2c8e6-104">WM\_GETMINMAXINFO message</span></span>

<span data-ttu-id="2c8e6-105">Enviado a uma janela quando o tamanho ou a posição da janela está prestes a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="2c8e6-105">Sent to a window when the size or position of the window is about to change.</span></span> <span data-ttu-id="2c8e6-106">Um aplicativo pode usar essa mensagem para substituir o tamanho e a posição padrão da janela, ou seu tamanho de rastreamento mínimo ou máximo padrão.</span><span class="sxs-lookup"><span data-stu-id="2c8e6-106">An application can use this message to override the window's default maximized size and position, or its default minimum or maximum tracking size.</span></span>

<span data-ttu-id="2c8e6-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2c8e6-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a><span data-ttu-id="2c8e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c8e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c8e6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c8e6-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="2c8e6-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2c8e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c8e6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c8e6-112">Um ponteiro para uma estrutura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contém a posição e dimensões maximizadas padrão e os tamanhos de rastreamento mínimo e máximo padrão.</span><span class="sxs-lookup"><span data-stu-id="2c8e6-112">A pointer to a [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) structure that contains the default maximized position and dimensions, and the default minimum and maximum tracking sizes.</span></span> <span data-ttu-id="2c8e6-113">Um aplicativo pode substituir os padrões definindo os membros dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="2c8e6-113">An application can override the defaults by setting the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8e6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c8e6-114">Return value</span></span>

<span data-ttu-id="2c8e6-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="2c8e6-115">Type: **LRESULT**</span></span>

<span data-ttu-id="2c8e6-116">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="2c8e6-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8e6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c8e6-117">Remarks</span></span>

<span data-ttu-id="2c8e6-118">O tamanho máximo de rastreamento é o maior tamanho de janela que pode ser produzido usando as bordas para dimensionar a janela.</span><span class="sxs-lookup"><span data-stu-id="2c8e6-118">The maximum tracking size is the largest window size that can be produced by using the borders to size the window.</span></span> <span data-ttu-id="2c8e6-119">O tamanho mínimo de rastreamento é o menor tamanho de janela que pode ser produzido usando as bordas para dimensionar a janela.</span><span class="sxs-lookup"><span data-stu-id="2c8e6-119">The minimum tracking size is the smallest window size that can be produced by using the borders to size the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8e6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c8e6-120">Requirements</span></span>



| <span data-ttu-id="2c8e6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c8e6-121">Requirement</span></span> | <span data-ttu-id="2c8e6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2c8e6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8e6-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c8e6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8e6-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c8e6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2c8e6-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c8e6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8e6-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c8e6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c8e6-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c8e6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c8e6-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c8e6-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8e6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c8e6-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c8e6-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2c8e6-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2c8e6-131">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="2c8e6-131">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="2c8e6-132">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="2c8e6-132">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="2c8e6-133">**MINMAXINFO**</span><span class="sxs-lookup"><span data-stu-id="2c8e6-133">**MINMAXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

<span data-ttu-id="2c8e6-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="2c8e6-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2c8e6-135">Windows</span><span class="sxs-lookup"><span data-stu-id="2c8e6-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
