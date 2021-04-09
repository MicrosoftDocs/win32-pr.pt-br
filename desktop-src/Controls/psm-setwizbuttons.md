---
title: Mensagem de PSM_SETWIZBUTTONS (Prsht. h)
description: Habilita ou desabilita os botões voltar, avançar e concluir em um assistente. Você também pode usar a \_ macro PropSheet SetWizButtons para postar a mensagem.
ms.assetid: e32abdb0-12d1-471e-a309-662389e0dba4
keywords:
- Controles de PSM_SETWIZBUTTONS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79cb7b6fbc0c91e1e94df62c2c8401839ace2d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085727"
---
# <a name="psm_setwizbuttons-message"></a><span data-ttu-id="1c511-105">Mensagem de PSM \_ SETWIZBUTTONS</span><span class="sxs-lookup"><span data-stu-id="1c511-105">PSM\_SETWIZBUTTONS message</span></span>

<span data-ttu-id="1c511-106">Habilita ou desabilita os botões **voltar**, **Avançar** e **concluir** em um assistente.</span><span class="sxs-lookup"><span data-stu-id="1c511-106">Enables or disables the **Back**, **Next**, and **Finish** buttons in a wizard.</span></span> <span data-ttu-id="1c511-107">Você também pode usar a macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para postar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1c511-107">You can also use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to post the message.</span></span>

## <a name="parameters"></a><span data-ttu-id="1c511-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c511-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c511-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c511-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c511-110">Defina esse parâmetro como PSWIZBF \_ ELEVATIONREQUIRED para exibir o ícone com privilégios elevados nos botões especificados em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1c511-110">Set this parameter to PSWIZBF\_ELEVATIONREQUIRED to display the elevated icon on the buttons specified in *lParam*.</span></span> <span data-ttu-id="1c511-111">O ícone com privilégios elevados (ou ícone de escudo do UAC) indica que o prompt de elevação será usado para solicitar a aprovação ou as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="1c511-111">The elevated icon (or UAC shield icon) indicates that the elevation prompt will be used to prompt the user for approval or credentials.</span></span> <span data-ttu-id="1c511-112">Para obter mais informações, consulte [criando aplicativos de UAC para o Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="1c511-112">For more information, see [Designing UAC Applications for Windows Vista]( /previous-versions/bb756973(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="1c511-113">Só há suporte para a exibição do ícone de escudo do UAC em AeroWizards (PSH \_ AEROWIZARD).</span><span class="sxs-lookup"><span data-stu-id="1c511-113">Displaying the UAC shield icon is only supported in AeroWizards (PSH\_AEROWIZARD).</span></span>

 

</dd> <dt>

<span data-ttu-id="1c511-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c511-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1c511-115">Valor que especifica quais botões de folha de propriedades estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="1c511-115">Value that specifies which property sheet buttons are enabled.</span></span> <span data-ttu-id="1c511-116">Você pode combinar um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c511-116">You can combine one or more of the following flags.</span></span>



| <span data-ttu-id="1c511-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1c511-117">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="1c511-118">Significado</span><span class="sxs-lookup"><span data-stu-id="1c511-118">Meaning</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <span data-ttu-id="1c511-119"><dt>**PSWIZB \_ voltar**</dt></span><span class="sxs-lookup"><span data-stu-id="1c511-119"><dt>**PSWIZB\_BACK**</dt></span></span> </dl>                               | <span data-ttu-id="1c511-120">Habilita o botão **voltar** .</span><span class="sxs-lookup"><span data-stu-id="1c511-120">Enables the **Back** button.</span></span> <span data-ttu-id="1c511-121">Se esse sinalizador não for definido, o botão **voltar** será exibido como desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1c511-121">If this flag is not set, the **Back** button is displayed as disabled.</span></span><br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <span data-ttu-id="1c511-122"><dt>**PSWIZB \_ DISABLEDFINISH**</dt></span><span class="sxs-lookup"><span data-stu-id="1c511-122"><dt>**PSWIZB\_DISABLEDFINISH**</dt></span></span> </dl> | <span data-ttu-id="1c511-123">Exibe um botão de **conclusão** desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1c511-123">Displays a disabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <span data-ttu-id="1c511-124"><dt>**PSWIZB \_ concluir**</dt></span><span class="sxs-lookup"><span data-stu-id="1c511-124"><dt>**PSWIZB\_FINISH**</dt></span></span> </dl>                         | <span data-ttu-id="1c511-125">Exibe um botão de **conclusão** habilitado.</span><span class="sxs-lookup"><span data-stu-id="1c511-125">Displays an enabled **Finish** button.</span></span><br/>                                                              |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <span data-ttu-id="1c511-126"><dt>**PSWIZB \_ próximo**</dt></span><span class="sxs-lookup"><span data-stu-id="1c511-126"><dt>**PSWIZB\_NEXT**</dt></span></span> </dl>                               | <span data-ttu-id="1c511-127">Habilita botão **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="1c511-127">Enables the **Next** button.</span></span> <span data-ttu-id="1c511-128">Se esse sinalizador não for definido, o botão **Avançar** será exibido como desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1c511-128">If this flag is not set, the **Next** button is displayed as disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c511-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c511-129">Return value</span></span>

<span data-ttu-id="1c511-130">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1c511-130">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c511-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c511-131">Remarks</span></span>

<span data-ttu-id="1c511-132">Se o seu [**manipulador de notificação**](/windows/desktop/api/winuser/nf-winuser-postmessagea) usar a ação executar para enviar uma mensagem de **PSM \_ SETWIZBUTTONS** , não faça nada que afete o foco da janela até que o manipulador retorne.</span><span class="sxs-lookup"><span data-stu-id="1c511-132">If your notification handler uses [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) to send a **PSM\_SETWIZBUTTONS** message, do nothing that will affect window focus until after the handler returns.</span></span> <span data-ttu-id="1c511-133">Por exemplo, se você chamar [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) imediatamente após usar a Execute para enviar **PSM \_ SETWIZBUTTONS**, a **caixa de mensagem** receberá o foco.</span><span class="sxs-lookup"><span data-stu-id="1c511-133">For example, if you call [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) immediately after using **PostMessage** to send **PSM\_SETWIZBUTTONS**, the message box will receive focus.</span></span> <span data-ttu-id="1c511-134">Como as mensagens postadas não são entregues até chegarem ao início da fila de mensagens, a mensagem de **PSM \_ SETWIZBUTTONS** não será entregue até que o assistente tenha perdido o foco na caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1c511-134">Since posted messages are not delivered until they reach the head of the message queue, the **PSM\_SETWIZBUTTONS** message will not be delivered until after the wizard has lost focus to the message box.</span></span> <span data-ttu-id="1c511-135">Como resultado, a folha de propriedades não poderá definir corretamente o foco para os botões.</span><span class="sxs-lookup"><span data-stu-id="1c511-135">As a result, the property sheet will not be able to properly set the focus for the buttons.</span></span>

<span data-ttu-id="1c511-136">Se você enviar a mensagem de PSM \_ SETWIZBUTTONS durante o tratamento da notificação [PSN \_ SetActive](psn-setactive.md) , use a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) em vez da função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="1c511-136">If you send the PSM\_SETWIZBUTTONS message during your handling of the [PSN\_SETACTIVE](psn-setactive.md) notification, use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function rather than the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="1c511-137">Caso contrário, o sistema não atualizará os botões corretamente.</span><span class="sxs-lookup"><span data-stu-id="1c511-137">Otherwise, the system will not update the buttons properly.</span></span> <span data-ttu-id="1c511-138">Se você usar a macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para enviar essa mensagem, ela será postada.</span><span class="sxs-lookup"><span data-stu-id="1c511-138">If you use the [**PropSheet\_SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) macro to send this message, it will be posted.</span></span> <span data-ttu-id="1c511-139">Em qualquer outro momento, você pode usar **SendMessage** para enviar **\_ SETWIZBUTTONS de PSM**.</span><span class="sxs-lookup"><span data-stu-id="1c511-139">At any other time, you can use **SendMessage** to send **PSM\_SETWIZBUTTONS**.</span></span>

<span data-ttu-id="1c511-140">Os assistentes exibem três ou quatro botões abaixo de cada página.</span><span class="sxs-lookup"><span data-stu-id="1c511-140">Wizards display either three or four buttons below each page.</span></span> <span data-ttu-id="1c511-141">Essa mensagem é usada para especificar quais botões estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="1c511-141">This message is used to specify which buttons are enabled.</span></span> <span data-ttu-id="1c511-142">Os assistentes normalmente exibem **voltar**, **Cancelar** e um botão **Avançar** ou **concluir** .</span><span class="sxs-lookup"><span data-stu-id="1c511-142">Wizards normally display **Back**, **Cancel**, and either a **Next** or **Finish** button.</span></span> <span data-ttu-id="1c511-143">Normalmente, você habilita apenas o botão **Avançar** para a página de boas-vindas, **próximo** e **voltar** para páginas interiores, e **voltar** e **concluir** para a página de conclusão.</span><span class="sxs-lookup"><span data-stu-id="1c511-143">You typically enable only the **Next** button for the welcome page, **Next** and **Back** for interior pages, and **Back** and **Finish** for the completion page.</span></span> <span data-ttu-id="1c511-144">O botão **Cancelar** está sempre habilitado.</span><span class="sxs-lookup"><span data-stu-id="1c511-144">The **Cancel** button is always enabled.</span></span> <span data-ttu-id="1c511-145">Normalmente, definir PSWIZB \_ Finish ou PSWIZB \_ DISABLEDFINISH substitui o botão **Next** por um botão **Finish** .</span><span class="sxs-lookup"><span data-stu-id="1c511-145">Normally, setting PSWIZB\_FINISH or PSWIZB\_DISABLEDFINISH replaces the **Next** button with a **Finish** button.</span></span> <span data-ttu-id="1c511-146">Para exibir os botões **Avançar** e **concluir** simultaneamente, defina o \_ sinalizador PSH WIZARDHASFINISH no membro **dwFlags** da estrutura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) do assistente ao criar o assistente.</span><span class="sxs-lookup"><span data-stu-id="1c511-146">To display **Next** and **Finish** buttons simultaneously, set the PSH\_WIZARDHASFINISH flag in the **dwFlags** member of the wizard's [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure when you create the wizard.</span></span> <span data-ttu-id="1c511-147">Cada página exibirá todos os quatro botões.</span><span class="sxs-lookup"><span data-stu-id="1c511-147">Every page will then display all four buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c511-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c511-148">Requirements</span></span>



| <span data-ttu-id="1c511-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c511-149">Requirement</span></span> | <span data-ttu-id="1c511-150">Valor</span><span class="sxs-lookup"><span data-stu-id="1c511-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c511-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c511-151">Minimum supported client</span></span><br/> | <span data-ttu-id="1c511-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c511-152">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1c511-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c511-153">Minimum supported server</span></span><br/> | <span data-ttu-id="1c511-154">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1c511-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1c511-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c511-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c511-156"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c511-156"><dt>Prsht.h</dt></span></span> </dl> |



 

