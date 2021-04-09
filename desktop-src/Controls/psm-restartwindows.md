---
title: Mensagem de PSM_RESTARTWINDOWS (Prsht. h)
description: Indica que o Windows precisa ser reiniciado para que as alterações entrem em vigor.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- Controles de PSM_RESTARTWINDOWS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824334"
---
# <a name="psm_restartwindows-message"></a><span data-ttu-id="e8b30-104">Mensagem de PSM \_ RESTARTWINDOWS</span><span class="sxs-lookup"><span data-stu-id="e8b30-104">PSM\_RESTARTWINDOWS message</span></span>

<span data-ttu-id="e8b30-105">Indica que o Windows precisa ser reiniciado para que as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="e8b30-105">Indicates that Windows needs to be restarted for the changes to take effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8b30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8b30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8b30-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8b30-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8b30-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e8b30-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e8b30-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8b30-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8b30-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e8b30-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8b30-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8b30-111">Return value</span></span>

<span data-ttu-id="e8b30-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e8b30-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8b30-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8b30-113">Remarks</span></span>

<span data-ttu-id="e8b30-114">Um aplicativo deve enviar essa mensagem somente em resposta ao código de notificação [PSN \_ Apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b30-114">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span> <span data-ttu-id="e8b30-115">Você pode enviar a mensagem de **PSM \_ RESTARTWINDOWS** explicitamente ou usando a macro [**PropSheet \_ RESTARTWINDOWS**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .</span><span class="sxs-lookup"><span data-stu-id="e8b30-115">You can send the **PSM\_RESTARTWINDOWS** message explicitly or by using the [**PropSheet\_RestartWindows**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) macro.</span></span>

<span data-ttu-id="e8b30-116">Essa mensagem faz com que a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retorne o \_ valor PSRESTARTWINDOWS da ID, mas somente se o usuário clicar no botão **OK** para fechar a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e8b30-116">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSRESTARTWINDOWS value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="e8b30-117">É responsabilidade do aplicativo reiniciar o Windows, o que pode ser feito usando a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="e8b30-117">It is the application's responsibility to restart Windows, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

> [!Note]  
> <span data-ttu-id="e8b30-118">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="e8b30-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8b30-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8b30-119">Requirements</span></span>



| <span data-ttu-id="e8b30-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8b30-120">Requirement</span></span> | <span data-ttu-id="e8b30-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e8b30-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b30-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8b30-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b30-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8b30-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e8b30-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8b30-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b30-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8b30-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8b30-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8b30-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8b30-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8b30-127"><dt>Prsht.h</dt></span></span> </dl> |



 

