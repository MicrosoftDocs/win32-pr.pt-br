---
title: Mensagem de WM_CTLCOLORDLG (WinUser. h)
description: Enviado para uma caixa de diálogo antes de o sistema desenhar a caixa de diálogo. Ao responder a essa mensagem, a caixa de diálogo pode definir suas cores de texto e de plano de fundo usando o identificador de contexto do dispositivo de vídeo especificado.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Caixas de diálogo de WM_CTLCOLORDLG mensagem
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644313"
---
# <a name="wm_ctlcolordlg-message"></a><span data-ttu-id="b9fc8-105">Mensagem do WM \_ CTLCOLORDLG</span><span class="sxs-lookup"><span data-stu-id="b9fc8-105">WM\_CTLCOLORDLG message</span></span>

<span data-ttu-id="b9fc8-106">Enviado para uma caixa de diálogo antes de o sistema desenhar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-106">Sent to a dialog box before the system draws the dialog box.</span></span> <span data-ttu-id="b9fc8-107">Ao responder a essa mensagem, a caixa de diálogo pode definir suas cores de texto e de plano de fundo usando o identificador de contexto do dispositivo de vídeo especificado.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-107">By responding to this message, the dialog box can set its text and background colors using the specified display device context handle.</span></span>


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a><span data-ttu-id="b9fc8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9fc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9fc8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9fc8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9fc8-110">Um identificador para o contexto do dispositivo para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-110">A handle to the device context for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b9fc8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9fc8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9fc8-112">Um identificador para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-112">A handle to the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9fc8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9fc8-113">Return value</span></span>

<span data-ttu-id="b9fc8-114">Se um aplicativo processar essa mensagem, ele deverá retornar um identificador para um pincel.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="b9fc8-115">O sistema usa o pincel para pintar o plano de fundo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-115">The system uses the brush to paint the background of the dialog box.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9fc8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9fc8-116">Remarks</span></span>

<span data-ttu-id="b9fc8-117">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the dialog box.</span></span>

<span data-ttu-id="b9fc8-118">O sistema não destrói automaticamente o pincel retornado.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-118">The system does not automatically destroy the returned brush.</span></span> <span data-ttu-id="b9fc8-119">É responsabilidade do aplicativo destruir o pincel quando ele não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-119">It is the application's responsibility to destroy the brush when it is no longer needed.</span></span>

<span data-ttu-id="b9fc8-120">A mensagem do **WM \_ CTLCOLORDLG** nunca é enviada entre threads.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-120">The **WM\_CTLCOLORDLG** message is never sent between threads.</span></span> <span data-ttu-id="b9fc8-121">Ele é enviado somente dentro de um thread.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-121">It is sent only within one thread.</span></span>

<span data-ttu-id="b9fc8-122">Observe que a mensagem do **WM \_ CTLCOLORDLG** é enviada para a própria caixa de diálogo; todas as outras mensagens do \**WM \_ CTLCOLOR \** _ são enviadas para o proprietário do controle.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-122">Note that the **WM\_CTLCOLORDLG** message is sent to the dialog box itself; all of the other \**WM\_CTLCOLOR\** _ messages are sent to the owner of the control.</span></span>

<span data-ttu-id="b9fc8-123">Se um procedimento da caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado em um _ *int \_ PTR*\* e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-123">If a dialog box procedure handles this message, it should cast the desired return value to an _ *INT\_PTR*\* and return the value directly.</span></span> <span data-ttu-id="b9fc8-124">Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-124">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="b9fc8-125">O valor de **\_ MSGRESULT DWL** definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="b9fc8-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9fc8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9fc8-126">Requirements</span></span>



| <span data-ttu-id="b9fc8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9fc8-127">Requirement</span></span> | <span data-ttu-id="b9fc8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b9fc8-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9fc8-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9fc8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9fc8-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9fc8-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b9fc8-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9fc8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9fc8-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9fc8-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b9fc8-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b9fc8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9fc8-134"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9fc8-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9fc8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9fc8-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9fc8-136">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b9fc8-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b9fc8-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b9fc8-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b9fc8-138">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="b9fc8-138">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="b9fc8-139">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b9fc8-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b9fc8-140">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="b9fc8-140">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="b9fc8-141">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="b9fc8-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b9fc8-142">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="b9fc8-142">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="b9fc8-143">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="b9fc8-143">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

