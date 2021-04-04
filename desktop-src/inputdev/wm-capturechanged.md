---
title: Mensagem de WM_CAPTURECHANGED (WinUser. h)
description: Enviado para a janela que está perdendo a captura do mouse.
ms.assetid: 79c8f65e-31fa-4bdb-9e88-0160a52b5b7d
keywords:
- Entrada de mouse e teclado de mensagem WM_CAPTURECHANGED
topic_type:
- apiref
api_name:
- WM_CAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050bc00a7ab19e22e0fe4ea1f35271707180d4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085426"
---
# <a name="wm_capturechanged-message"></a><span data-ttu-id="51952-104">Mensagem do WM \_ capturachanged</span><span class="sxs-lookup"><span data-stu-id="51952-104">WM\_CAPTURECHANGED message</span></span>

<span data-ttu-id="51952-105">Enviado para a janela que está perdendo a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="51952-105">Sent to the window that is losing the mouse capture.</span></span>

<span data-ttu-id="51952-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="51952-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CAPTURECHANGED               0x0215
```



## <a name="parameters"></a><span data-ttu-id="51952-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51952-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51952-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51952-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51952-109">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="51952-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="51952-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51952-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51952-111">Um identificador para a janela que ganha a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="51952-111">A handle to the window gaining the mouse capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51952-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51952-112">Return value</span></span>

<span data-ttu-id="51952-113">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="51952-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="51952-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="51952-114">Remarks</span></span>

<span data-ttu-id="51952-115">Uma janela recebe essa mensagem, mesmo que chame o próprio [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) .</span><span class="sxs-lookup"><span data-stu-id="51952-115">A window receives this message even if it calls [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) itself.</span></span> <span data-ttu-id="51952-116">Um aplicativo não deve tentar definir a captura do mouse em resposta a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="51952-116">An application should not attempt to set the mouse capture in response to this message.</span></span>

<span data-ttu-id="51952-117">Quando ele recebe essa mensagem, uma janela deve ser redesenhada, se necessário, para refletir o novo estado de captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="51952-117">When it receives this message, a window should redraw itself, if necessary, to reflect the new mouse-capture state.</span></span>

## <a name="requirements"></a><span data-ttu-id="51952-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51952-118">Requirements</span></span>



| <span data-ttu-id="51952-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="51952-119">Requirement</span></span> | <span data-ttu-id="51952-120">Valor</span><span class="sxs-lookup"><span data-stu-id="51952-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51952-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51952-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51952-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51952-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="51952-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51952-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51952-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51952-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="51952-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="51952-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="51952-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51952-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51952-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="51952-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="51952-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="51952-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51952-129">**ReleaseCapture**</span><span class="sxs-lookup"><span data-stu-id="51952-129">**ReleaseCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

[<span data-ttu-id="51952-130">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="51952-130">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="51952-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="51952-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51952-132">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="51952-132">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

