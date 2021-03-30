---
title: PSN_APPLY código de notificação (Prsht. h)
description: Enviado a cada página na folha de propriedades para indicar que o usuário clicou no botão OK, fechar ou aplicar e quer que todas as alterações entrem em vigor. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d8206b4e423fb01be3277a9dd0ca3a49b59129
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455423"
---
# <a name="psn_apply-notification-code"></a><span data-ttu-id="a8a74-105">PSN \_ aplicar código de notificação</span><span class="sxs-lookup"><span data-stu-id="a8a74-105">PSN\_APPLY notification code</span></span>

<span data-ttu-id="a8a74-106">Enviado a cada página na folha de propriedades para indicar que o usuário clicou no botão OK, fechar ou aplicar e quer que todas as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="a8a74-106">Sent to every page in the property sheet to indicate that the user has clicked the OK, Close, or Apply button and wants all changes to take effect.</span></span> <span data-ttu-id="a8a74-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a8a74-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a8a74-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8a74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a74-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8a74-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a74-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação, incluindo a ID da página.</span><span class="sxs-lookup"><span data-stu-id="a8a74-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code, including the ID of the page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a74-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8a74-111">Return value</span></span>

<span data-ttu-id="a8a74-112">Defina PSNRET \_ NOERROR para indicar que as alterações feitas nesta página são válidas e foram aplicadas.</span><span class="sxs-lookup"><span data-stu-id="a8a74-112">Set PSNRET\_NOERROR to indicate that the changes made to this page are valid and have been applied.</span></span> <span data-ttu-id="a8a74-113">Se todas as páginas definirem PSNRET \_ NOERROR, a folha de propriedades poderá ser destruída.</span><span class="sxs-lookup"><span data-stu-id="a8a74-113">If all pages set PSNRET\_NOERROR, the property sheet can be destroyed.</span></span> <span data-ttu-id="a8a74-114">Para indicar que as alterações feitas nesta página são inválidas e para impedir que a folha de propriedades seja destruída, defina um dos seguintes valores de retorno:</span><span class="sxs-lookup"><span data-stu-id="a8a74-114">To indicate that the changes made to this page are invalid and to prevent the property sheet from being destroyed, set one of the following return values:</span></span>

-   <span data-ttu-id="a8a74-115">PSNRET \_ inválido.</span><span class="sxs-lookup"><span data-stu-id="a8a74-115">PSNRET\_INVALID.</span></span> <span data-ttu-id="a8a74-116">A folha de propriedades não será destruída e o foco será retornado para esta página.</span><span class="sxs-lookup"><span data-stu-id="a8a74-116">The property sheet will not be destroyed, and focus will be returned to this page.</span></span>
-   <span data-ttu-id="a8a74-117">PSNRET \_ NOCHANGEPAGE inválida \_ .</span><span class="sxs-lookup"><span data-stu-id="a8a74-117">PSNRET\_INVALID\_NOCHANGEPAGE.</span></span> <span data-ttu-id="a8a74-118">A folha de propriedades não será destruída e o foco será retornado para a página que tinha o foco quando o botão foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="a8a74-118">The property sheet will not be destroyed, and focus will be returned to the page that had focus when the button was pressed.</span></span>

<span data-ttu-id="a8a74-119">Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor MSGRESULT DWL e o procedimento da caixa de diálogo deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="a8a74-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8a74-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8a74-120">Remarks</span></span>

<span data-ttu-id="a8a74-121">Quando o usuário clica no botão OK, aplicar ou fechar, a folha de propriedades envia uma notificação [PSN \_ KILLACTIVE](psn-killactive.md) para a página ativa, dando a ela uma oportunidade de validar as alterações do usuário.</span><span class="sxs-lookup"><span data-stu-id="a8a74-121">When the user clicks the OK, Apply, or Close button, the property sheet sends a [PSN\_KILLACTIVE](psn-killactive.md) notification to the active page, giving it an opportunity to validate the user's changes.</span></span> <span data-ttu-id="a8a74-122">Se as alterações forem válidas, a folha de propriedades enviará um \_ código de notificação PSN aplicar a cada página, direcionando-a para aplicar as novas propriedades ao item correspondente.</span><span class="sxs-lookup"><span data-stu-id="a8a74-122">If the changes are valid, the property sheet sends a PSN\_APPLY notification code to each page, directing it to apply the new properties to the corresponding item.</span></span>

> [!Note]  
> <span data-ttu-id="a8a74-123">A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação PSN aplicar é enviado.</span><span class="sxs-lookup"><span data-stu-id="a8a74-123">The property sheet is in the process of manipulating the list of pages when the PSN\_APPLY notification code is sent.</span></span> <span data-ttu-id="a8a74-124">Não tente adicionar, remover ou inserir páginas enquanto manipula essa notificação.</span><span class="sxs-lookup"><span data-stu-id="a8a74-124">Do not attempt to add, remove, or insert pages while handling this notification.</span></span> <span data-ttu-id="a8a74-125">Isso terá resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="a8a74-125">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="a8a74-126">O membro **lParam** da estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) apontada por *lParam* será definido como **true** se o usuário clicar no botão OK.</span><span class="sxs-lookup"><span data-stu-id="a8a74-126">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* is set to **TRUE** if the user clicks the OK button.</span></span> <span data-ttu-id="a8a74-127">Ele também será definido como **true** se a mensagem de [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md) tiver sido enviada e o usuário clicar no botão fechar.</span><span class="sxs-lookup"><span data-stu-id="a8a74-127">It is also set to **TRUE** if the [**PSM\_CANCELTOCLOSE**](psm-canceltoclose.md) message has been sent and the user clicks the Close button.</span></span> <span data-ttu-id="a8a74-128">Ele será definido como **false** se o usuário clicar no botão Aplicar.</span><span class="sxs-lookup"><span data-stu-id="a8a74-128">It is set to **FALSE** if the user clicks the Apply button.</span></span>

<span data-ttu-id="a8a74-129">A estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a8a74-129">The [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="a8a74-130">Não chame a função [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) ao processar este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="a8a74-130">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

<span data-ttu-id="a8a74-131">Uma folha de propriedades modal é destruída se o usuário clica no botão OK e cada página retorna o \_ valor de NOERROR PSNRET em resposta a **PSN \_ Apply**.</span><span class="sxs-lookup"><span data-stu-id="a8a74-131">A modal property sheet is destroyed if the user clicks the OK button and every page returns the PSNRET\_NOERROR value in response to **PSN\_APPLY**.</span></span> <span data-ttu-id="a8a74-132">Se qualquer página retornar PSNRET \_ inválido ou PSNRET \_ \_ NOCHANGEPAGE inválido, o processo de aplicação será cancelado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a8a74-132">If any page returns PSNRET\_INVALID or PSNRET\_INVALID\_NOCHANGEPAGE, the Apply process is canceled immediately.</span></span> <span data-ttu-id="a8a74-133">As páginas após a página de cancelamento não receberão um \_ código de notificação PSN aplicar.</span><span class="sxs-lookup"><span data-stu-id="a8a74-133">Pages after the cancelling page will not receive a PSN\_APPLY notification code.</span></span>

<span data-ttu-id="a8a74-134">Para receber esse código de notificação, uma página deve definir o \_ valor DWL MSGRESULT como **false** em resposta ao código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="a8a74-134">To receive this notification code, a page must set the DWL\_MSGRESULT value to **FALSE** in response to the [PSN\_KILLACTIVE](psn-killactive.md) notification code.</span></span>

> [!Note]  
> <span data-ttu-id="a8a74-135">Não há suporte para este código de notificação ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="a8a74-135">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a8a74-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8a74-136">Requirements</span></span>



| <span data-ttu-id="a8a74-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8a74-137">Requirement</span></span> | <span data-ttu-id="a8a74-138">Valor</span><span class="sxs-lookup"><span data-stu-id="a8a74-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a74-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8a74-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a8a74-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8a74-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a8a74-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8a74-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a8a74-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8a74-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a8a74-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8a74-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8a74-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8a74-144"><dt>Prsht.h</dt></span></span> </dl> |



 

