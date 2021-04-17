---
title: Mensagem de PSM_SHOWWIZBUTTONS (Prsht. h)
description: Mostra ou oculta botões em um assistente. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ ShowWizButtons.
ms.assetid: 669c4e51-cac1-40e1-8f23-afae0e41fc9b
keywords:
- Controles de PSM_SHOWWIZBUTTONS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SHOWWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e8d1fc54d556240ef3fa6d6b6185a669978b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754808"
---
# <a name="psm_showwizbuttons-message"></a><span data-ttu-id="6e746-105">Mensagem de PSM \_ SHOWWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="6e746-105">PSM\_SHOWWIZBUTTONS message</span></span>

<span data-ttu-id="6e746-106">Mostra ou oculta botões em um assistente.</span><span class="sxs-lookup"><span data-stu-id="6e746-106">Shows or hides buttons in a wizard.</span></span> <span data-ttu-id="6e746-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) .</span><span class="sxs-lookup"><span data-stu-id="6e746-107">You can send this message explicitly or by using the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e746-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e746-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e746-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e746-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e746-110">Um ou mais dos valores a seguir que especificam quais botões de folha de propriedades devem ser mostrados.</span><span class="sxs-lookup"><span data-stu-id="6e746-110">One or more of the following values that specify which property sheet buttons are to be shown.</span></span> <span data-ttu-id="6e746-111">Se um valor de botão for incluído nesse parâmetro e no *lParam*, ele será mostrado.</span><span class="sxs-lookup"><span data-stu-id="6e746-111">If a button value is included in both this parameter and *lParam*, it is shown.</span></span>



| <span data-ttu-id="6e746-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6e746-112">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="6e746-113">Significado</span><span class="sxs-lookup"><span data-stu-id="6e746-113">Meaning</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="6e746-114"><dt>**PSWIZB \_ voltar**</dt></span><span class="sxs-lookup"><span data-stu-id="6e746-114"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="6e746-115">O botão **voltar** .</span><span class="sxs-lookup"><span data-stu-id="6e746-115">The **Back** button.</span></span><br/>                                                            |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <span data-ttu-id="6e746-116"><dt>**PSWIZB \_ cancelar**</dt></span><span class="sxs-lookup"><span data-stu-id="6e746-116"><dt>**PSWIZB\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="6e746-117">O botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="6e746-117">The **Cancel** button.</span></span><br/>                                                          |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="6e746-118"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="6e746-118"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="6e746-119">O botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="6e746-119">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="6e746-120"><dt>**PSWIZB \_ concluir**</dt></span><span class="sxs-lookup"><span data-stu-id="6e746-120"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="6e746-121">O botão **concluir** .</span><span class="sxs-lookup"><span data-stu-id="6e746-121">The **Finish** button.</span></span><br/>                                                          |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="6e746-122"><dt>**PSWIZB \_ próximo**</dt></span><span class="sxs-lookup"><span data-stu-id="6e746-122"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="6e746-123">O botão **Avançar** .</span><span class="sxs-lookup"><span data-stu-id="6e746-123">The **Next** button.</span></span><br/>                                                            |
| <span id="PSWIZB_SHOW"></span><span id="pswizb_show"></span><dl> <span data-ttu-id="6e746-124"><dt>**PSWIZB \_ Mostrar**</dt></span><span class="sxs-lookup"><span data-stu-id="6e746-124"><dt>**PSWIZB\_SHOW**</dt></span></span> </dl>                               | <span data-ttu-id="6e746-125">Defina somente este sinalizador (definido como zero) para ocultar todos os botões especificados em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6e746-125">Set only this flag (defined as zero) to hide all buttons specified in *lParam*.</span></span><br/> |
| <span id="PSWIZB_RESTORE"></span><span id="pswizb_restore"></span><dl> <span data-ttu-id="6e746-126"><dt>**PSWIZB \_ restauração**</dt></span><span class="sxs-lookup"><span data-stu-id="6e746-126"><dt>**PSWIZB\_RESTORE**</dt></span></span> </dl>                      | <span data-ttu-id="6e746-127">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="6e746-127">Not implemented.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="6e746-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e746-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e746-129">Um ou mais dos mesmos valores usados em *wParam*, especificando quais botões são afetados por essa chamada.</span><span class="sxs-lookup"><span data-stu-id="6e746-129">One or more of the same values used in *wParam*, specifying which buttons are affected by this call.</span></span> <span data-ttu-id="6e746-130">Se um valor de botão aparecer nesse parâmetro, mas não em *wParam*, o botão ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="6e746-130">If a button value appears in this parameter but not in *wParam*, the button is hidden.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e746-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e746-131">Return value</span></span>

<span data-ttu-id="6e746-132">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6e746-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e746-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e746-133">Remarks</span></span>

<span data-ttu-id="6e746-134">Os assistentes exibem três ou quatro botões abaixo de cada página.</span><span class="sxs-lookup"><span data-stu-id="6e746-134">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="6e746-135">Essa mensagem é usada para especificar quais botões estão visíveis.</span><span class="sxs-lookup"><span data-stu-id="6e746-135">This message is used to specify which buttons are visible.</span></span> <span data-ttu-id="6e746-136">Os assistentes normalmente exibem **voltar**, **Cancelar** e um botão **Avançar** ou **concluir** .</span><span class="sxs-lookup"><span data-stu-id="6e746-136">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="6e746-137">O botão **Cancelar** está sempre visível.</span><span class="sxs-lookup"><span data-stu-id="6e746-137">The **Cancel** button is always visible.</span></span>

<span data-ttu-id="6e746-138">Normalmente, defina **PSWIZB \_ Finish** ou **PSWIZB \_ DISABLEDFINISH** para substituir o botão **Next** por um botão **Finish** .</span><span class="sxs-lookup"><span data-stu-id="6e746-138">Typically, set **PSWIZB\_FINISH** or **PSWIZB\_DISABLEDFINISH** to replace the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="6e746-139">Para exibir os botões **Avançar** e **concluir** simultaneamente, defina o sinalizador **PSH \_ WIZARDHASFINISH** no membro **dwFlags** da estrutura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) ao criar o assistente.</span><span class="sxs-lookup"><span data-stu-id="6e746-139">To display **Next** and **Finish** buttons simultaneously, set the **PSH\_WIZARDHASFINISH** flag in the **dwFlags** member of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="6e746-140">Cada página exibirá todos os quatro botões: **voltar**, **Avançar**, **Cancelar** e **concluir**.</span><span class="sxs-lookup"><span data-stu-id="6e746-140">Every page will then display all four buttons: **Back**, **Next**, **Cancel**, and **Finish**.</span></span>

<span data-ttu-id="6e746-141">Se você usar a macro [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) para enviar essa mensagem, ela será postada.</span><span class="sxs-lookup"><span data-stu-id="6e746-141">If you use the [**PropSheet\_ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="6e746-142">Em qualquer outro momento, você pode usar [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar **\_ SHOWWIZBUTTONS de PSM**.</span><span class="sxs-lookup"><span data-stu-id="6e746-142">At any other time, you can use [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to send **PSM\_SHOWWIZBUTTONS**.</span></span>

<span data-ttu-id="6e746-143">Se o seu [**manipulador de notificação**](/windows/desktop/api/winuser/nf-winuser-postmessagea) usar a ação executar para enviar uma mensagem de **PSM \_ SHOWWIZBUTTONS** , não faça nada que afete o foco da janela até que o manipulador retorne.</span><span class="sxs-lookup"><span data-stu-id="6e746-143">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SHOWWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="6e746-144">Por exemplo, se você chamar [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) imediatamente após usar a Execute para enviar **PSM \_ SHOWWIZBUTTONS**, a **caixa de mensagem** receberá o foco.</span><span class="sxs-lookup"><span data-stu-id="6e746-144">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SHOWWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="6e746-145">Como as mensagens postadas não são entregues até chegarem ao início da fila de mensagens, a mensagem de **PSM \_ SHOWWIZBUTTONS** não será entregue até que o assistente tenha perdido o foco na caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e746-145">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SHOWWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="6e746-146">Como resultado, a folha de propriedades não poderá definir corretamente o foco para os botões.</span><span class="sxs-lookup"><span data-stu-id="6e746-146">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e746-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e746-147">Requirements</span></span>



| <span data-ttu-id="6e746-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e746-148">Requirement</span></span> | <span data-ttu-id="6e746-149">Valor</span><span class="sxs-lookup"><span data-stu-id="6e746-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e746-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e746-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6e746-151">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e746-151">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6e746-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e746-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6e746-153">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e746-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6e746-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e746-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e746-155"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e746-155"><dt>Prsht.h</dt></span></span> </dl> |



 

