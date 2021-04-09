---
title: Mensagem de PSM_CANCELTOCLOSE (Prsht. h)
description: Enviado por um aplicativo quando ele realizou alterações desde a notificação de aplicação de PSN mais recente \_ que não pode ser cancelada. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- Controles de PSM_CANCELTOCLOSE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086088"
---
# <a name="psm_canceltoclose-message"></a><span data-ttu-id="ba8b5-105">Mensagem de PSM \_ CANCELTOCLOSE</span><span class="sxs-lookup"><span data-stu-id="ba8b5-105">PSM\_CANCELTOCLOSE message</span></span>

<span data-ttu-id="ba8b5-106">Enviado por um aplicativo quando ele realizou alterações desde a notificação de [ \_ aplicação de PSN](psn-apply.md) mais recente que não pode ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-106">Sent by an application when it has performed changes since the most recent [PSN\_APPLY](psn-apply.md) notification that cannot be canceled.</span></span> <span data-ttu-id="ba8b5-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .</span><span class="sxs-lookup"><span data-stu-id="ba8b5-107">You can send this message explicitly or by using the [**PropSheet\_CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba8b5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba8b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba8b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba8b5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba8b5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba8b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba8b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba8b5-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba8b5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba8b5-113">Return value</span></span>

<span data-ttu-id="ba8b5-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8b5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba8b5-115">Remarks</span></span>

<span data-ttu-id="ba8b5-116">**PSM \_ CANCELTOCLOSE** desabilita o botão **Cancelar** e altera o texto do botão **OK** para "fechar".</span><span class="sxs-lookup"><span data-stu-id="ba8b5-116">**PSM\_CANCELTOCLOSE** disables the **Cancel** button and changes the text of the **OK** button to "Close".</span></span>

<span data-ttu-id="ba8b5-117">A maioria das folhas de propriedades aguarda a execução de alterações irreversíveis até que uma notificação de aplicação de PSN \_ seja recebida.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-117">Most property sheets wait to perform irreversible changes until a PSN\_APPLY notification is received.</span></span> <span data-ttu-id="ba8b5-118">No entanto, em algumas circunstâncias, uma folha de propriedades pode fazer alterações irreversíveis fora da \_ sequência de redefinição de aplicação/PSN padrão PSN \_ .</span><span class="sxs-lookup"><span data-stu-id="ba8b5-118">However, in some circumstances, a property sheet may make irreversible changes outside the standard PSN\_APPLY/PSN\_RESET sequence.</span></span> <span data-ttu-id="ba8b5-119">Um exemplo é uma folha de propriedades que contém um botão de **edição** que é usado para exibir uma caixa de diálogo para editar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-119">One example is a property sheet that contains an **Edit** button that is used to display a subdialog box for editing a property.</span></span> <span data-ttu-id="ba8b5-120">Quando o usuário clica em **OK** para enviar a alteração, a página da folha de propriedades tem várias opções.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-120">When the user clicks **OK** to submit the change, the property sheet page has several options.</span></span>

-   <span data-ttu-id="ba8b5-121">Ele pode registrar as alterações, mas aguarde até receber uma notificação de \_ aplicação de PSN para aplicá-las.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-121">It can record the changes, but wait until it receives a PSN\_APPLY notification to apply them.</span></span> <span data-ttu-id="ba8b5-122">Essa é a abordagem preferida.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-122">This is the preferred approach.</span></span>
-   <span data-ttu-id="ba8b5-123">Ele pode aplicar as alterações imediatamente após sair da caixa de diálogo, mas lembre-se das configurações originais.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-123">It can apply the changes immediately after exiting the subdialog box, but remember the original settings.</span></span> <span data-ttu-id="ba8b5-124">Essas configurações podem ser usadas para restaurar o estado original se uma \_ notificação de redefinição de PSN for recebida.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-124">Those settings can be used to restore the original state if a PSN\_RESET notification is received.</span></span>
-   <span data-ttu-id="ba8b5-125">Ele pode aplicar as alterações imediatamente e não tentar restaurar as configurações originais quando receber uma notificação de [ \_ redefinição de PSN](psn-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="ba8b5-125">It can apply the changes immediately and not attempt to restore the original settings when it receives a [PSN\_RESET](psn-reset.md) notification.</span></span> <span data-ttu-id="ba8b5-126">Essa abordagem não é recomendada, mas pode ser necessária se as alterações estiverem muito longe para que as outras duas opções sejam práticas.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-126">This approach is not recommended, but may be necessary if the changes are too far-reaching for the other two options to be practical.</span></span>

<span data-ttu-id="ba8b5-127">Para a terceira opção, os aplicativos devem enviar uma mensagem de **PSM \_ CANCELTOCLOSE** para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ba8b5-127">For the third option, applications should send a **PSM\_CANCELTOCLOSE** message to the property sheet.</span></span> <span data-ttu-id="ba8b5-128">Ele indica ao usuário que as alterações feitas com a caixa de diálogo não podem ser revertidas clicando no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="ba8b5-128">It indicates to the user that the changes made with the subdialog box cannot be reversed by clicking the **Cancel** button.</span></span>

> [!Note]  
> <span data-ttu-id="ba8b5-129">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="ba8b5-129">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba8b5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba8b5-130">Requirements</span></span>



| <span data-ttu-id="ba8b5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba8b5-131">Requirement</span></span> | <span data-ttu-id="ba8b5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="ba8b5-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8b5-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba8b5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ba8b5-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba8b5-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ba8b5-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba8b5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ba8b5-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba8b5-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ba8b5-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba8b5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba8b5-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba8b5-138"><dt>Prsht.h</dt></span></span> </dl> |



 

 





