---
title: Mensagem de WM_ENTERIDLE (WinUser. h)
description: Enviado para a janela do proprietário de uma caixa de diálogo modal ou um menu que está entrando em um estado ocioso. Uma caixa de diálogo modal ou um menu entra em estado ocioso quando nenhuma mensagem está aguardando em sua fila depois de ter processado uma ou mais mensagens anteriores.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- Caixas de diálogo de WM_ENTERIDLE mensagem
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369805"
---
# <a name="wm_enteridle-message"></a><span data-ttu-id="ebf9d-105">Mensagem do WM \_ ENTERIDLE</span><span class="sxs-lookup"><span data-stu-id="ebf9d-105">WM\_ENTERIDLE message</span></span>

<span data-ttu-id="ebf9d-106">Enviado para a janela do proprietário de uma caixa de diálogo modal ou um menu que está entrando em um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-106">Sent to the owner window of a modal dialog box or menu that is entering an idle state.</span></span> <span data-ttu-id="ebf9d-107">Uma caixa de diálogo modal ou um menu entra em estado ocioso quando nenhuma mensagem está aguardando em sua fila depois de ter processado uma ou mais mensagens anteriores.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-107">A modal dialog box or menu enters an idle state when no messages are waiting in its queue after it has processed one or more previous messages.</span></span>


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a><span data-ttu-id="ebf9d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebf9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf9d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ebf9d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf9d-110">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ebf9d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ebf9d-111">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="ebf9d-112">Significado</span><span class="sxs-lookup"><span data-stu-id="ebf9d-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <span data-ttu-id="ebf9d-113"><dt>**MSGF \_ CAIXA**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ebf9d-113"><dt>**MSGF\_DIALOGBOX**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="ebf9d-114">O sistema está ocioso porque uma caixa de diálogo é exibida.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-114">The system is idle because a dialog box is displayed.</span></span><br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <span data-ttu-id="ebf9d-115"><dt>**MSGF \_ MENU**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ebf9d-115"><dt>**MSGF\_MENU**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="ebf9d-116">O sistema está ocioso porque um menu é exibido.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-116">The system is idle because a menu is displayed.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="ebf9d-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebf9d-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebf9d-118">Um identificador para a caixa de diálogo (se *wParam* for **MSGF \_ caixa**) ou janela que contém o menu exibido (se *wParam* for **MSGF \_ menu**).</span><span class="sxs-lookup"><span data-stu-id="ebf9d-118">A handle to the dialog box (if *wParam* is **MSGF\_DIALOGBOX**) or window containing the displayed menu (if *wParam* is **MSGF\_MENU**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf9d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ebf9d-119">Return value</span></span>

<span data-ttu-id="ebf9d-120">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-120">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebf9d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebf9d-121">Remarks</span></span>

<span data-ttu-id="ebf9d-122">Você pode suprimir a mensagem do **WM \_ ENTERIDLE** para uma caixa de diálogo criando a caixa de diálogo com o estilo de **\_ NOIDLEMSG do DS** .</span><span class="sxs-lookup"><span data-stu-id="ebf9d-122">You can suppress the **WM\_ENTERIDLE** message for a dialog box by creating the dialog box with the **DS\_NOIDLEMSG** style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf9d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebf9d-123">Requirements</span></span>



| <span data-ttu-id="ebf9d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebf9d-124">Requirement</span></span> | <span data-ttu-id="ebf9d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ebf9d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebf9d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf9d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf9d-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ebf9d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ebf9d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebf9d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf9d-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ebf9d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ebf9d-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ebf9d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebf9d-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebf9d-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebf9d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebf9d-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="ebf9d-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ebf9d-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="ebf9d-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ebf9d-136">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="ebf9d-136">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

