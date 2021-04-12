---
title: PSN_WIZFINISH código de notificação (Prsht. h)
description: Notifica uma página que o usuário clicou no botão concluir em um assistente. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0654384b0944d90731288922c32326e42019cdc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455538"
---
# <a name="psn_wizfinish-notification-code"></a><span data-ttu-id="89735-105">Código de notificação do PSN \_ WIZFINISH</span><span class="sxs-lookup"><span data-stu-id="89735-105">PSN\_WIZFINISH notification code</span></span>

<span data-ttu-id="89735-106">Notifica uma página que o usuário clicou no botão **concluir** em um assistente.</span><span class="sxs-lookup"><span data-stu-id="89735-106">Notifies a page that the user has clicked the **Finish** button in a wizard.</span></span> <span data-ttu-id="89735-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="89735-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="89735-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89735-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89735-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89735-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89735-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="89735-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="89735-111">Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="89735-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="89735-112">O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="89735-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89735-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89735-113">Return value</span></span>

-   <span data-ttu-id="89735-114">Retorna **true** para impedir que o assistente seja concluído.</span><span class="sxs-lookup"><span data-stu-id="89735-114">Returns **TRUE** to prevent the wizard from finishing.</span></span>
-   [<span data-ttu-id="89735-115">Versão 5,80.</span><span class="sxs-lookup"><span data-stu-id="89735-115">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="89735-116">e posterior.</span><span class="sxs-lookup"><span data-stu-id="89735-116">and later.</span></span> <span data-ttu-id="89735-117">Retorna um identificador de janela para impedir que o assistente seja concluído.</span><span class="sxs-lookup"><span data-stu-id="89735-117">Returns a window handle to prevent the wizard from finishing.</span></span> <span data-ttu-id="89735-118">O assistente definirá o foco para essa janela.</span><span class="sxs-lookup"><span data-stu-id="89735-118">The wizard will set the focus to that window.</span></span> <span data-ttu-id="89735-119">A janela deve pertencer à página do assistente.</span><span class="sxs-lookup"><span data-stu-id="89735-119">The window must be owned by the wizard page.</span></span>
-   <span data-ttu-id="89735-120">Retorna **false** para permitir que o assistente seja concluído.</span><span class="sxs-lookup"><span data-stu-id="89735-120">Returns **FALSE** to allow the wizard to finish.</span></span>

## <a name="remarks"></a><span data-ttu-id="89735-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="89735-121">Remarks</span></span>

<span data-ttu-id="89735-122">Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor MSGRESULT DWL e o procedimento da caixa de diálogo deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="89735-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

[<span data-ttu-id="89735-123">Versão 5,80.</span><span class="sxs-lookup"><span data-stu-id="89735-123">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="89735-124">Se seu aplicativo retornar **true** para impedir que um assistente seja concluído, ele não terá controle sobre qual janela na página recebe o foco.</span><span class="sxs-lookup"><span data-stu-id="89735-124">If your application returns **TRUE** to prevent a wizard from finishing, it has no control over which window on the page receives focus.</span></span> <span data-ttu-id="89735-125">Os aplicativos que precisam parar a conclusão de um assistente normalmente devem fazer isso retornando o identificador da janela na página do assistente que deve receber o foco.</span><span class="sxs-lookup"><span data-stu-id="89735-125">Applications that need to stop a wizard from finishing should normally do so by returning the handle of the window on the wizard page that is to receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="89735-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89735-126">Requirements</span></span>



| <span data-ttu-id="89735-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="89735-127">Requirement</span></span> | <span data-ttu-id="89735-128">Valor</span><span class="sxs-lookup"><span data-stu-id="89735-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89735-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89735-129">Minimum supported client</span></span><br/> | <span data-ttu-id="89735-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89735-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="89735-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89735-131">Minimum supported server</span></span><br/> | <span data-ttu-id="89735-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89735-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89735-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89735-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="89735-134"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="89735-134"><dt>Prsht.h</dt></span></span> </dl> |



 

