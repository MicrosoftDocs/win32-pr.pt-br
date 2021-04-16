---
description: Enviado a uma janela após a função SetWindowLong ter alterado um ou mais dos estilos da janela.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: Mensagem de WM_STYLECHANGED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506121"
---
# <a name="wm_stylechanged-message"></a><span data-ttu-id="c3f6e-103">Mensagem de estilo do WM \_</span><span class="sxs-lookup"><span data-stu-id="c3f6e-103">WM\_STYLECHANGED message</span></span>

<span data-ttu-id="c3f6e-104">Enviado a uma janela após a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ter alterado um ou mais dos estilos da janela.</span><span class="sxs-lookup"><span data-stu-id="c3f6e-104">Sent to a window after the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function has changed one or more of the window's styles.</span></span>

<span data-ttu-id="c3f6e-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c3f6e-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a><span data-ttu-id="c3f6e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3f6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f6e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3f6e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3f6e-108">Indica se os estilos da janela ou os estilos de janela estendidos foram alterados.</span><span class="sxs-lookup"><span data-stu-id="c3f6e-108">Indicates whether the window's styles or extended window styles have changed.</span></span> <span data-ttu-id="c3f6e-109">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3f6e-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="c3f6e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c3f6e-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="c3f6e-111">Significado</span><span class="sxs-lookup"><span data-stu-id="c3f6e-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="c3f6e-112"><dt>**GWL \_ Filestyle**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="c3f6e-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="c3f6e-113">Os estilos de janela estendidos foram alterados.</span><span class="sxs-lookup"><span data-stu-id="c3f6e-113">The extended window styles have changed.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="c3f6e-114"><dt>**GWL \_ ESTILO**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="c3f6e-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="c3f6e-115">Os estilos de janela foram alterados.</span><span class="sxs-lookup"><span data-stu-id="c3f6e-115">The window styles have changed.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="c3f6e-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3f6e-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3f6e-117">Um ponteiro para uma estrutura [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contém os novos estilos para a janela.</span><span class="sxs-lookup"><span data-stu-id="c3f6e-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the new styles for the window.</span></span> <span data-ttu-id="c3f6e-118">Um aplicativo pode examinar os estilos, mas não pode alterá-los.</span><span class="sxs-lookup"><span data-stu-id="c3f6e-118">An application can examine the styles, but cannot change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f6e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3f6e-119">Return value</span></span>

<span data-ttu-id="c3f6e-120">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c3f6e-120">Type: **LRESULT**</span></span>

<span data-ttu-id="c3f6e-121">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3f6e-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f6e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3f6e-122">Requirements</span></span>



| <span data-ttu-id="c3f6e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3f6e-123">Requirement</span></span> | <span data-ttu-id="c3f6e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c3f6e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f6e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3f6e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f6e-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3f6e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c3f6e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3f6e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f6e-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3f6e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c3f6e-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c3f6e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3f6e-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f6e-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f6e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3f6e-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3f6e-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c3f6e-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3f6e-133">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="c3f6e-133">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[<span data-ttu-id="c3f6e-134">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="c3f6e-134">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="c3f6e-135">**STYLECHANGING do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c3f6e-135">**WM\_STYLECHANGING**</span></span>](wm-stylechanging.md)
</dt> <dt>

<span data-ttu-id="c3f6e-136">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c3f6e-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c3f6e-137">Windows</span><span class="sxs-lookup"><span data-stu-id="c3f6e-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
