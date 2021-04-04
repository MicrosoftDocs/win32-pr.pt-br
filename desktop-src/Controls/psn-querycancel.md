---
title: PSN_QUERYCANCEL código de notificação (Prsht. h)
description: Indica que o usuário cancelou a folha de propriedades. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918340"
---
# <a name="psn_querycancel-notification-code"></a><span data-ttu-id="b5206-105">Código de notificação do PSN \_ QUERYCANCEL</span><span class="sxs-lookup"><span data-stu-id="b5206-105">PSN\_QUERYCANCEL notification code</span></span>

<span data-ttu-id="b5206-106">Indica que o usuário cancelou a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5206-106">Indicates that the user has canceled the property sheet.</span></span> <span data-ttu-id="b5206-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b5206-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a><span data-ttu-id="b5206-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5206-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5206-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5206-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5206-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="b5206-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="b5206-111">Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5206-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="b5206-112">O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="b5206-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5206-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5206-113">Return value</span></span>

<span data-ttu-id="b5206-114">Retorna **true** para impedir a operação de cancelamento ou **false** para permiti-la.</span><span class="sxs-lookup"><span data-stu-id="b5206-114">Returns **TRUE** to prevent the cancel operation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5206-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5206-115">Remarks</span></span>

<span data-ttu-id="b5206-116">Esse código de notificação normalmente é enviado quando um usuário clica no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="b5206-116">This notification code is typically sent when a user clicks the **Cancel** button.</span></span> <span data-ttu-id="b5206-117">Ele também é enviado quando um usuário clica no botão **X** no canto superior direito da folha de propriedades ou pressiona a tecla escape.</span><span class="sxs-lookup"><span data-stu-id="b5206-117">It is also sent when a user clicks the **X** button in the property sheet's upper right hand corner or presses the ESCAPE key.</span></span> <span data-ttu-id="b5206-118">Uma página de folha de propriedades pode manipular esse código de notificação para solicitar que o usuário Verifique a operação de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="b5206-118">A property sheet page can handle this notification code to ask the user to verify the cancel operation.</span></span>

<span data-ttu-id="b5206-119">Para definir um valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com DWL \_ MSGRESULT definido como o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b5206-119">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT set to the return value.</span></span> <span data-ttu-id="b5206-120">O procedimento da caixa de diálogo deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="b5206-120">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5206-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5206-121">Requirements</span></span>



| <span data-ttu-id="b5206-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5206-122">Requirement</span></span> | <span data-ttu-id="b5206-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b5206-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5206-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5206-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b5206-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5206-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b5206-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5206-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b5206-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5206-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5206-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5206-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5206-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5206-129"><dt>Prsht.h</dt></span></span> </dl> |



 

