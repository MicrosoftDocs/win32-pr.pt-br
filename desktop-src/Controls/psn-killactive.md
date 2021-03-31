---
title: PSN_KILLACTIVE código de notificação (Prsht. h)
description: Notifica uma página de que ela está prestes a perder a ativação porque outra página está sendo ativada ou o usuário clicou no botão OK. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918342"
---
# <a name="psn_killactive-notification-code"></a><span data-ttu-id="bab61-105">Código de notificação do PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="bab61-105">PSN\_KILLACTIVE notification code</span></span>

<span data-ttu-id="bab61-106">Notifica uma página de que ela está prestes a perder a ativação porque outra página está sendo ativada ou o usuário clicou no botão OK.</span><span class="sxs-lookup"><span data-stu-id="bab61-106">Notifies a page that it is about to lose activation either because another page is being activated or the user has clicked the OK button.</span></span> <span data-ttu-id="bab61-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bab61-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bab61-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bab61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bab61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bab61-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab61-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="bab61-111">Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bab61-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="bab61-112">O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="bab61-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab61-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bab61-113">Return value</span></span>

<span data-ttu-id="bab61-114">Retorna **true** para impedir que a página perca a ativação ou **false** para permiti-la.</span><span class="sxs-lookup"><span data-stu-id="bab61-114">Returns **TRUE** to prevent the page from losing the activation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab61-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bab61-115">Remarks</span></span>

<span data-ttu-id="bab61-116">Um aplicativo manipula esse código de notificação para validar as informações inseridas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bab61-116">An application handles this notification code to validate the information the user has entered.</span></span>

> [!Note]  
> <span data-ttu-id="bab61-117">A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação PSN KILLACTIVE é enviado.</span><span class="sxs-lookup"><span data-stu-id="bab61-117">The property sheet is in the process of manipulating the list of pages when the PSN\_KILLACTIVE notification code is sent.</span></span> <span data-ttu-id="bab61-118">Não tente adicionar, remover ou inserir páginas enquanto manipula este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="bab61-118">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="bab61-119">Isso terá resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="bab61-119">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="bab61-120">Para definir um valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com um \_ valor DWL MSGRESULT definido como o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="bab61-120">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a DWL\_MSGRESULT value set to the return value.</span></span> <span data-ttu-id="bab61-121">O procedimento da caixa de diálogo deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="bab61-121">The dialog box procedure must return **TRUE**.</span></span>

<span data-ttu-id="bab61-122">Se o procedimento da caixa de diálogo Definir DWL \_ MSGRESULT como **true**, ele deverá exibir uma caixa de mensagem para explicar o problema ao usuário.</span><span class="sxs-lookup"><span data-stu-id="bab61-122">If the dialog box procedure sets DWL\_MSGRESULT to **TRUE**, it should display a message box to explain the problem to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="bab61-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bab61-123">Requirements</span></span>



| <span data-ttu-id="bab61-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab61-124">Requirement</span></span> | <span data-ttu-id="bab61-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bab61-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bab61-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bab61-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bab61-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bab61-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bab61-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bab61-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bab61-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bab61-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bab61-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bab61-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bab61-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab61-131"><dt>Prsht.h</dt></span></span> </dl> |



 

