---
title: Mensagem de WM_GETHOTKEY (WinUser. h)
description: Enviado para determinar a tecla de acesso associada a uma janela.
ms.assetid: 6f527758-e713-47a8-a571-3bf3270f0b33
keywords:
- Entrada de mouse e teclado de mensagem WM_GETHOTKEY
topic_type:
- apiref
api_name:
- WM_GETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f045ceefaf33c8d8edba0cb69e062ad589cfd833
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454960"
---
# <a name="wm_gethotkey-message"></a><span data-ttu-id="62642-104">Mensagem de autotecla do WM \_</span><span class="sxs-lookup"><span data-stu-id="62642-104">WM\_GETHOTKEY message</span></span>

<span data-ttu-id="62642-105">Enviado para determinar a tecla de acesso associada a uma janela.</span><span class="sxs-lookup"><span data-stu-id="62642-105">Sent to determine the hot key associated with a window.</span></span>


```C++
#define WM_GETHOTKEY                    0x0033
```



## <a name="parameters"></a><span data-ttu-id="62642-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62642-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62642-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62642-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62642-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="62642-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="62642-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62642-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62642-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="62642-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62642-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62642-111">Return value</span></span>

<span data-ttu-id="62642-112">O valor de retorno é o código de chave virtual e os modificadores para a tecla de acesso, ou **NULL** se nenhuma tecla de acesso estiver associada à janela.</span><span class="sxs-lookup"><span data-stu-id="62642-112">The return value is the virtual-key code and modifiers for the hot key, or **NULL** if no hot key is associated with the window.</span></span> <span data-ttu-id="62642-113">O código de chave virtual está no byte baixo do valor de retorno e os modificadores estão no byte alto.</span><span class="sxs-lookup"><span data-stu-id="62642-113">The virtual-key code is in the low byte of the return value and the modifiers are in the high byte.</span></span> <span data-ttu-id="62642-114">Os modificadores podem ser uma combinação dos seguintes sinalizadores de CommCtrl. h.</span><span class="sxs-lookup"><span data-stu-id="62642-114">The modifiers can be a combination of the following flags from CommCtrl.h.</span></span>



| <span data-ttu-id="62642-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="62642-115">Return code/value</span></span>                                                                                                                                         | <span data-ttu-id="62642-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="62642-116">Description</span></span>             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="62642-117"><dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="62642-117"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>     | <span data-ttu-id="62642-118">tecla ALT</span><span class="sxs-lookup"><span data-stu-id="62642-118">ALT key</span></span><br/>      |
| <dl> <span data-ttu-id="62642-119"><dt>**HOTKEYF \_ CONTROLE**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="62642-119"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="62642-120">Tecla CTRL</span><span class="sxs-lookup"><span data-stu-id="62642-120">CTRL key</span></span><br/>     |
| <dl> <span data-ttu-id="62642-121"><dt>**HOTKEYF \_**</dt> <dt>0x08</dt> ext.</span><span class="sxs-lookup"><span data-stu-id="62642-121"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>     | <span data-ttu-id="62642-122">Chave estendida</span><span class="sxs-lookup"><span data-stu-id="62642-122">Extended key</span></span><br/> |
| <dl> <span data-ttu-id="62642-123"><dt>**HOTKEYF \_ SHIFT**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="62642-123"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>   | <span data-ttu-id="62642-124">Tecla SHIFT</span><span class="sxs-lookup"><span data-stu-id="62642-124">SHIFT key</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="62642-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="62642-125">Remarks</span></span>

<span data-ttu-id="62642-126">Essas teclas de acesso não estão relacionadas às teclas de acesso definidas pela função [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) .</span><span class="sxs-lookup"><span data-stu-id="62642-126">These hot keys are unrelated to the hot keys set by the [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="62642-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62642-127">Requirements</span></span>



| <span data-ttu-id="62642-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="62642-128">Requirement</span></span> | <span data-ttu-id="62642-129">Valor</span><span class="sxs-lookup"><span data-stu-id="62642-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62642-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62642-130">Minimum supported client</span></span><br/> | <span data-ttu-id="62642-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="62642-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="62642-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62642-132">Minimum supported server</span></span><br/> | <span data-ttu-id="62642-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="62642-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62642-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="62642-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="62642-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62642-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62642-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="62642-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="62642-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="62642-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="62642-138">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="62642-138">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="62642-139">**WM \_ SETtecla de atalho**</span><span class="sxs-lookup"><span data-stu-id="62642-139">**WM\_SETHOTKEY**</span></span>](wm-sethotkey.md)
</dt> <dt>

<span data-ttu-id="62642-140">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="62642-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62642-141">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="62642-141">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

