---
description: Enviado a uma janela quando a função SetWindowLong está prestes a alterar um ou mais dos estilos da janela.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: Mensagem de WM_STYLECHANGING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828447"
---
# <a name="wm_stylechanging-message"></a><span data-ttu-id="4a0fd-103">Mensagem do WM \_ STYLECHANGING</span><span class="sxs-lookup"><span data-stu-id="4a0fd-103">WM\_STYLECHANGING message</span></span>

<span data-ttu-id="4a0fd-104">Enviado a uma janela quando a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) está prestes a alterar um ou mais dos estilos da janela.</span><span class="sxs-lookup"><span data-stu-id="4a0fd-104">Sent to a window when the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is about to change one or more of the window's styles.</span></span>

<span data-ttu-id="4a0fd-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4a0fd-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a><span data-ttu-id="4a0fd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a0fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a0fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a0fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a0fd-108">Indica se os estilos da janela ou os estilos de janela estendidos estão sendo alterados.</span><span class="sxs-lookup"><span data-stu-id="4a0fd-108">Indicates whether the window's styles or extended window styles are changing.</span></span> <span data-ttu-id="4a0fd-109">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a0fd-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="4a0fd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="4a0fd-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="4a0fd-111">Significado</span><span class="sxs-lookup"><span data-stu-id="4a0fd-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="4a0fd-112"><dt>**GWL \_ Filestyle**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="4a0fd-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="4a0fd-113">Os estilos de janela estendidos estão sendo alterados.</span><span class="sxs-lookup"><span data-stu-id="4a0fd-113">The extended window styles are changing.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="4a0fd-114"><dt>**GWL \_ ESTILO**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="4a0fd-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="4a0fd-115">Os estilos de janela estão sendo alterados.</span><span class="sxs-lookup"><span data-stu-id="4a0fd-115">The window styles are changing.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="4a0fd-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a0fd-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a0fd-117">Um ponteiro para uma estrutura [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) que contém os novos estilos propostos para a janela.</span><span class="sxs-lookup"><span data-stu-id="4a0fd-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the proposed new styles for the window.</span></span> <span data-ttu-id="4a0fd-118">Um aplicativo pode examinar os estilos e, se necessário, alterá-los.</span><span class="sxs-lookup"><span data-stu-id="4a0fd-118">An application can examine the styles and, if necessary, change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a0fd-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a0fd-119">Return value</span></span>

<span data-ttu-id="4a0fd-120">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a0fd-120">Type: **LRESULT**</span></span>

<span data-ttu-id="4a0fd-121">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="4a0fd-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a0fd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a0fd-122">Requirements</span></span>



| <span data-ttu-id="4a0fd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a0fd-123">Requirement</span></span> | <span data-ttu-id="4a0fd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4a0fd-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a0fd-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a0fd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4a0fd-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a0fd-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4a0fd-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a0fd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4a0fd-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a0fd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a0fd-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4a0fd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a0fd-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a0fd-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a0fd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a0fd-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a0fd-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4a0fd-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4a0fd-133">**STYLESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="4a0fd-133">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="4a0fd-134">**estilo do WMchanged \_**</span><span class="sxs-lookup"><span data-stu-id="4a0fd-134">**WM\_STYLECHANGED**</span></span>](wm-stylechanged.md)
</dt> <dt>

<span data-ttu-id="4a0fd-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4a0fd-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4a0fd-136">Windows</span><span class="sxs-lookup"><span data-stu-id="4a0fd-136">Windows</span></span>](windows.md)
</dt> </dl>

 

 
