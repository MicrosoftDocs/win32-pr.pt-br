---
title: PSN_SETACTIVE código de notificação (Prsht. h)
description: Notifica uma página que está prestes a ser ativada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918697"
---
# <a name="psn_setactive-notification-code"></a><span data-ttu-id="76081-105">\_Código de notificação PSN SETactive</span><span class="sxs-lookup"><span data-stu-id="76081-105">PSN\_SETACTIVE notification code</span></span>

<span data-ttu-id="76081-106">Notifica uma página que está prestes a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="76081-106">Notifies a page that it is about to be activated.</span></span> <span data-ttu-id="76081-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="76081-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="76081-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76081-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76081-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76081-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76081-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="76081-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="76081-111">Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="76081-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="76081-112">O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="76081-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76081-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76081-113">Return value</span></span>

<span data-ttu-id="76081-114">Retorna zero para aceitar a ativação ou-1 para ativar a próxima ou a página anterior (dependendo se o usuário clicou no botão **próximo** ou **voltar** ).</span><span class="sxs-lookup"><span data-stu-id="76081-114">Returns zero to accept the activation, or -1 to activate the next or the previous page (depending on whether the user clicked the **Next** or **Back** button).</span></span> <span data-ttu-id="76081-115">Para definir a ativação para uma página específica, retorne o identificador de recurso da página.</span><span class="sxs-lookup"><span data-stu-id="76081-115">To set the activation to a particular page, return the resource identifier of the page.</span></span>

## <a name="remarks"></a><span data-ttu-id="76081-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="76081-116">Remarks</span></span>

<span data-ttu-id="76081-117">O \_ código de notificação PSN SetActive é enviado antes que a página fique visível.</span><span class="sxs-lookup"><span data-stu-id="76081-117">The PSN\_SETACTIVE notification code is sent before the page is visible.</span></span> <span data-ttu-id="76081-118">Um aplicativo pode usar esse código de notificação para inicializar dados na página.</span><span class="sxs-lookup"><span data-stu-id="76081-118">An application can use this notification code to initialize data in the page.</span></span>

> [!Note]  
> <span data-ttu-id="76081-119">A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação SETactive da PSN é enviado.</span><span class="sxs-lookup"><span data-stu-id="76081-119">The property sheet is in the process of manipulating the list of pages when the PSN\_SETACTIVE notification code is sent.</span></span> <span data-ttu-id="76081-120">Não tente adicionar, remover ou inserir páginas enquanto manipula este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="76081-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="76081-121">Isso terá resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="76081-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="76081-122">Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor MSGRESULT DWL e o procedimento da caixa de diálogo deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="76081-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="76081-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76081-123">Requirements</span></span>



| <span data-ttu-id="76081-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="76081-124">Requirement</span></span> | <span data-ttu-id="76081-125">Valor</span><span class="sxs-lookup"><span data-stu-id="76081-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76081-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76081-126">Minimum supported client</span></span><br/> | <span data-ttu-id="76081-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76081-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="76081-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76081-128">Minimum supported server</span></span><br/> | <span data-ttu-id="76081-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76081-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="76081-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76081-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="76081-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="76081-131"><dt>Prsht.h</dt></span></span> </dl> |



 

