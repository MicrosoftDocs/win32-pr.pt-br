---
title: Mensagem de PSM_APPLY (Prsht. h)
description: Simula a seleção do botão aplicar, indicando que uma ou mais páginas foram alteradas e que as alterações precisam ser validadas e registradas.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- Controles de PSM_APPLY de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824636"
---
# <a name="psm_apply-message"></a><span data-ttu-id="807b2-104">Mensagem de aplicação de PSM \_</span><span class="sxs-lookup"><span data-stu-id="807b2-104">PSM\_APPLY message</span></span>

<span data-ttu-id="807b2-105">Simula a seleção do botão **aplicar** , indicando que uma ou mais páginas foram alteradas e que as alterações precisam ser validadas e registradas.</span><span class="sxs-lookup"><span data-stu-id="807b2-105">Simulates the selection of the **Apply** button, indicating that one or more pages have changed and the changes need to be validated and recorded.</span></span>

## <a name="parameters"></a><span data-ttu-id="807b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="807b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="807b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="807b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="807b2-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="807b2-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="807b2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="807b2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="807b2-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="807b2-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="807b2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="807b2-111">Return value</span></span>

<span data-ttu-id="807b2-112">Retornará **true** se todas as páginas forem aplicadas com êxito às alterações ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="807b2-112">Returns **TRUE** if all pages successfully applied the changes, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="807b2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="807b2-113">Remarks</span></span>

<span data-ttu-id="807b2-114">A folha de propriedades envia o código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) para a página atual.</span><span class="sxs-lookup"><span data-stu-id="807b2-114">The property sheet sends the [PSN\_KILLACTIVE](psn-killactive.md) notification code to the current page.</span></span> <span data-ttu-id="807b2-115">Se a página atual retornar **false**, a folha de propriedades enviará o código de notificação [PSN \_ aplicar](psn-apply.md) a todas as páginas ativas.</span><span class="sxs-lookup"><span data-stu-id="807b2-115">If the current page returns **FALSE**, the property sheet sends the [PSN\_APPLY](psn-apply.md) notification code to all active pages.</span></span> <span data-ttu-id="807b2-116">Você pode enviar a mensagem de PSM \_ Apply explicitamente ou usando a macro [**PropSheet \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .</span><span class="sxs-lookup"><span data-stu-id="807b2-116">You can send the PSM\_APPLY message explicitly or by using the [**PropSheet\_Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) macro.</span></span>

> [!Note]  
> <span data-ttu-id="807b2-117">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="807b2-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="807b2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="807b2-118">Requirements</span></span>



| <span data-ttu-id="807b2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="807b2-119">Requirement</span></span> | <span data-ttu-id="807b2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="807b2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="807b2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="807b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="807b2-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="807b2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="807b2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="807b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="807b2-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="807b2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="807b2-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="807b2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="807b2-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="807b2-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





