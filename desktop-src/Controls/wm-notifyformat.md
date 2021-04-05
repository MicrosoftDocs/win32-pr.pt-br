---
title: Mensagem de WM_NOTIFYFORMAT (WinUser. h)
description: Determina se uma janela aceita estruturas ANSI ou Unicode na mensagem de \_ notificação do WM Notify. \_As mensagens do WM NOTIFYFORMAT são enviadas de um controle comum para sua janela pai e da janela pai para o controle comum.
ms.assetid: 45ddef45-3300-448d-b609-5fe931b08336
keywords:
- Controles de WM_NOTIFYFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_NOTIFYFORMAT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e9c7d74b21d0f5785273d1b60d612a346f2d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918691"
---
# <a name="wm_notifyformat-message"></a><span data-ttu-id="c1dcb-105">Mensagem do WM \_ NOTIFYFORMAT</span><span class="sxs-lookup"><span data-stu-id="c1dcb-105">WM\_NOTIFYFORMAT message</span></span>

<span data-ttu-id="c1dcb-106">Determina se uma janela aceita estruturas ANSI ou Unicode na mensagem de notificação do [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1dcb-106">Determines if a window accepts ANSI or Unicode structures in the [**WM\_NOTIFY**](wm-notify.md) notification message.</span></span> <span data-ttu-id="c1dcb-107">**WM \_** As mensagens NOTIFYFORMAT são enviadas de um controle comum para sua janela pai e da janela pai para o controle comum.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-107">**WM\_NOTIFYFORMAT** messages are sent from a common control to its parent window and from the parent window to the common control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1dcb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1dcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1dcb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1dcb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1dcb-110">Um identificador para a janela que está enviando a **mensagem \_ NOTIFYFORMAT do WM** .</span><span class="sxs-lookup"><span data-stu-id="c1dcb-110">A handle to the window that is sending the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="c1dcb-111">Se *lParam* for NF \_ , esse parâmetro será o identificador para um controle.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-111">If *lParam* is NF\_QUERY, this parameter is the handle to a control.</span></span> <span data-ttu-id="c1dcb-112">Se *lParam* for NF \_ RepetirConsulta, esse parâmetro será o identificador para a janela pai de um controle.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-112">If *lParam* is NF\_REQUERY, this parameter is the handle to the parent window of a control.</span></span>

</dd> <dt>

<span data-ttu-id="c1dcb-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1dcb-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1dcb-114">O valor do comando que especifica a natureza da mensagem do **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="c1dcb-114">The command value that specifies the nature of the **WM\_NOTIFYFORMAT** message.</span></span> <span data-ttu-id="c1dcb-115">Esse será um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c1dcb-115">This will be one of the following values:</span></span>



| <span data-ttu-id="c1dcb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c1dcb-116">Value</span></span>                                                                                                                                                | <span data-ttu-id="c1dcb-117">Significado</span><span class="sxs-lookup"><span data-stu-id="c1dcb-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NF_QUERY"></span><span id="nf_query"></span><dl> <span data-ttu-id="c1dcb-118"><dt>**consulta de NF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1dcb-118"><dt>**NF\_QUERY**</dt></span></span> </dl>       | <span data-ttu-id="c1dcb-119">A mensagem é uma consulta para determinar se as estruturas ANSI ou Unicode devem ser usadas em mensagens de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1dcb-119">The message is a query to determine whether ANSI or Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="c1dcb-120">Esse comando é enviado de um controle para sua janela pai durante a criação de um controle e em resposta a um comando de NF- \_ repetição.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-120">This command is sent from a control to its parent window during the creation of a control and in response to an NF\_REQUERY command.</span></span><br/>                                                                                                         |
| <span id="NF_REQUERY"></span><span id="nf_requery"></span><dl> <span data-ttu-id="c1dcb-121"><dt>**reconsulta de NF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1dcb-121"><dt>**NF\_REQUERY**</dt></span></span> </dl> | <span data-ttu-id="c1dcb-122">A mensagem é uma solicitação de um controle para enviar um \_ formulário de consulta de NF dessa mensagem para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-122">The message is a request for a control to send an NF\_QUERY form of this message to its parent window.</span></span> <span data-ttu-id="c1dcb-123">Esse comando é enviado da janela pai.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-123">This command is sent from the parent window.</span></span> <span data-ttu-id="c1dcb-124">A janela pai está solicitando que o controle refaça a consulta sobre o tipo de estruturas a serem usadas nas mensagens de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1dcb-124">The parent window is asking the control to requery it about the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="c1dcb-125">Se *lParam* for NF \_ RepetirConsulta, o valor de retorno será o resultado da operação de consulta.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-125">If *lParam* is NF\_REQUERY, the return value is the result of the requery operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1dcb-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1dcb-126">Return value</span></span>

<span data-ttu-id="c1dcb-127">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-127">Returns one of the following values.</span></span>



| <span data-ttu-id="c1dcb-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c1dcb-128">Return code</span></span>                                                                                 | <span data-ttu-id="c1dcb-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1dcb-129">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1dcb-130"><dt>**NFR \_ ANSI**</dt></span><span class="sxs-lookup"><span data-stu-id="c1dcb-130"><dt>**NFR\_ANSI**</dt></span></span> </dl>    | <span data-ttu-id="c1dcb-131">As estruturas ANSI devem ser usadas em mensagens de [**\_ notificação do WM**](wm-notify.md) enviadas pelo controle.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-131">ANSI structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span><br/>     |
| <dl> <span data-ttu-id="c1dcb-132"><dt>**NFR \_ Unicode**</dt></span><span class="sxs-lookup"><span data-stu-id="c1dcb-132"><dt>**NFR\_UNICODE**</dt></span></span> </dl> | <span data-ttu-id="c1dcb-133">As estruturas Unicode devem ser usadas em mensagens de [**\_ notificação do WM**](wm-notify.md) enviadas pelo controle.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-133">Unicode structures should be used in [**WM\_NOTIFY**](wm-notify.md) messages sent by the control.</span></span> <br/> |
| <dl> <span data-ttu-id="c1dcb-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c1dcb-134"><dt>**0**</dt></span></span> </dl>            | <span data-ttu-id="c1dcb-135">Ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-135">An error occurred.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="c1dcb-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1dcb-136">Remarks</span></span>

<span data-ttu-id="c1dcb-137">Quando um controle comum é criado, o controle envia uma mensagem do **WM \_ NOTIFYFORMAT** para sua janela pai para determinar o tipo de estruturas a serem usadas nas mensagens de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1dcb-137">When a common control is created, the control sends a **WM\_NOTIFYFORMAT** message to its parent window to determine the type of structures to use in [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="c1dcb-138">Se a janela pai não tratar essa mensagem, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) responderá de acordo com o tipo da janela pai.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-138">If the parent window does not handle this message, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function responds according to the type of the parent window.</span></span> <span data-ttu-id="c1dcb-139">Ou seja, se a janela pai for uma janela Unicode, **DefWindowProc** retornará NFR \_ Unicode e, se a janela pai for uma janela ANSI, **DefWindowProc** retornará NFR \_ ANSI.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-139">That is, if the parent window is a Unicode window, **DefWindowProc** returns NFR\_UNICODE, and if the parent window is an ANSI window, **DefWindowProc** returns NFR\_ANSI.</span></span> <span data-ttu-id="c1dcb-140">Se a janela pai for uma caixa de diálogo e não tratar essa mensagem, a função [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) responderá de acordo com o tipo da caixa de diálogo (Unicode ou ANSI).</span><span class="sxs-lookup"><span data-stu-id="c1dcb-140">If the parent window is a dialog box and does not handle this message, the [**DefDlgProc**](/windows/desktop/api/winuser/nf-winuser-defdlgprocw) function similarly responds according to the type of the dialog box (Unicode or ANSI).</span></span>

<span data-ttu-id="c1dcb-141">Uma janela pai pode alterar o tipo de estruturas que um controle comum usa no [**WM \_ notificar**](wm-notify.md) mensagens definindo *lParam* para NF \_ RepetirConsulta e enviando uma mensagem do **WM \_ NOTIFYFORMAT** para o controle.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-141">A parent window can change the type of structures a common control uses in [**WM\_NOTIFY**](wm-notify.md) messages by setting *lParam* to NF\_REQUERY and sending a **WM\_NOTIFYFORMAT** message to the control.</span></span> <span data-ttu-id="c1dcb-142">Isso faz com que o controle envie um \_ formulário de consulta de NF da mensagem do **WM \_ NOTIFYFORMAT** para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-142">This causes the control to send an NF\_QUERY form of the **WM\_NOTIFYFORMAT** message to the parent window.</span></span>

<span data-ttu-id="c1dcb-143">Todos os controles comuns enviarão mensagens do **WM \_ NOTIFYFORMAT** .</span><span class="sxs-lookup"><span data-stu-id="c1dcb-143">All common controls will send **WM\_NOTIFYFORMAT** messages.</span></span> <span data-ttu-id="c1dcb-144">No entanto, os controles padrão do Windows (editar controles, caixas de combinação, caixas de listagem, botões, barras de rolagem e controles estáticos) não fazem isso.</span><span class="sxs-lookup"><span data-stu-id="c1dcb-144">However, the standard Windows controls (edit controls, combo boxes, list boxes, buttons, scroll bars, and static controls) do not.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1dcb-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1dcb-145">Requirements</span></span>



| <span data-ttu-id="c1dcb-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1dcb-146">Requirement</span></span> | <span data-ttu-id="c1dcb-147">Valor</span><span class="sxs-lookup"><span data-stu-id="c1dcb-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1dcb-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1dcb-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c1dcb-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1dcb-149">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c1dcb-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1dcb-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c1dcb-151">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1dcb-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c1dcb-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1dcb-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1dcb-153"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1dcb-153"><dt>Winuser.h</dt></span></span> </dl> |



 

