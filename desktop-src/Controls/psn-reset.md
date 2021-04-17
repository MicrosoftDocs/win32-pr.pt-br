---
title: PSN_RESET código de notificação (Prsht. h)
description: Notifica uma página que a folha de propriedades está prestes a ser destruída. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748254"
---
# <a name="psn_reset-notification-code"></a><span data-ttu-id="25691-105">\_Código de notificação de redefinição de PSN</span><span class="sxs-lookup"><span data-stu-id="25691-105">PSN\_RESET notification code</span></span>

<span data-ttu-id="25691-106">Notifica uma página que a folha de propriedades está prestes a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="25691-106">Notifies a page that the property sheet is about to be destroyed.</span></span> <span data-ttu-id="25691-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="25691-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="25691-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25691-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25691-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25691-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25691-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="25691-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25691-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25691-111">Return value</span></span>

<span data-ttu-id="25691-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="25691-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25691-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="25691-113">Remarks</span></span>

<span data-ttu-id="25691-114">Todas as alterações feitas desde o último código de notificação de [ \_ aplicação de PSN](psn-apply.md) são canceladas, exceto no caso de [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), que não oferece suporte a esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="25691-114">All changes made since the last [PSN\_APPLY](psn-apply.md) notification code are canceled, except in the case of [**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), which does not support that notification code.</span></span>

<span data-ttu-id="25691-115">O membro **lParam** da estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) apontada por *lParam* será definido como **true** se o usuário clicar no botão **X** no canto superior direito da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="25691-115">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* will be set to **TRUE** if the user clicked the **X** button in the upper-right corner of the property sheet.</span></span> <span data-ttu-id="25691-116">Será **false** se o usuário clicou no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="25691-116">It will be **FALSE** if the user clicked the **Cancel** button.</span></span> <span data-ttu-id="25691-117">A estrutura **PSHNOTIFY** contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="25691-117">The **PSHNOTIFY** structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="25691-118">Um aplicativo pode usar esse código de notificação como uma oportunidade para executar operações de limpeza.</span><span class="sxs-lookup"><span data-stu-id="25691-118">An application can use this notification code as an opportunity to perform cleanup operations.</span></span>

> [!Note]  
> <span data-ttu-id="25691-119">A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação de redefinição de PSN é enviado.</span><span class="sxs-lookup"><span data-stu-id="25691-119">The property sheet is in the process of manipulating the list of pages when the PSN\_RESET notification code is sent.</span></span> <span data-ttu-id="25691-120">Não tente adicionar, remover ou inserir páginas enquanto manipula este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="25691-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="25691-121">Isso terá resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="25691-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="25691-122">Não chame a função [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) ao processar este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="25691-122">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="25691-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25691-123">Requirements</span></span>



| <span data-ttu-id="25691-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="25691-124">Requirement</span></span> | <span data-ttu-id="25691-125">Valor</span><span class="sxs-lookup"><span data-stu-id="25691-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25691-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25691-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25691-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25691-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="25691-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25691-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25691-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25691-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="25691-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25691-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="25691-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="25691-131"><dt>Prsht.h</dt></span></span> </dl> |



 

