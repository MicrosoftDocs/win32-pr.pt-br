---
title: PSN_TRANSLATEACCELERATOR código de notificação (Prsht. h)
description: Notifica uma folha de propriedades de que uma mensagem do teclado foi recebida. Ele fornece à página uma oportunidade de fazer a tradução do acelerador de teclado privado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811139"
---
# <a name="psn_translateaccelerator-notification-code"></a><span data-ttu-id="bb400-106">\_Código de notificação PSN TRANSLATEACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="bb400-106">PSN\_TRANSLATEACCELERATOR notification code</span></span>

<span data-ttu-id="bb400-107">Notifica uma folha de propriedades de que uma mensagem do teclado foi recebida.</span><span class="sxs-lookup"><span data-stu-id="bb400-107">Notifies a property sheet that a keyboard message has been received.</span></span> <span data-ttu-id="bb400-108">Ele fornece à página uma oportunidade de fazer a tradução do acelerador de teclado privado.</span><span class="sxs-lookup"><span data-stu-id="bb400-108">It provides the page an opportunity to do private keyboard accelerator translation.</span></span> <span data-ttu-id="bb400-109">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bb400-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bb400-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb400-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb400-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb400-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb400-112">Um ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="bb400-112">A pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="bb400-113">Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** da estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bb400-113">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of the **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="bb400-114">O membro **lParam** da estrutura **PSHNOTIFY** é um ponteiro para a [**msg**](/windows/win32/api/winuser/ns-winuser-msg)da mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb400-114">The **lParam** member of the **PSHNOTIFY** structure is a pointer to the message's [**MSG**](/windows/win32/api/winuser/ns-winuser-msg).</span></span> <span data-ttu-id="bb400-115">Ele pode ser convertido em um tipo **LPMSG** para obter acesso aos parâmetros da mensagem a ser traduzida.</span><span class="sxs-lookup"><span data-stu-id="bb400-115">It can be cast to an **LPMSG** type, to get access to the parameters of the message to be translated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb400-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb400-116">Return value</span></span>

<span data-ttu-id="bb400-117">Retorna PSNRET \_ MESSAGEHANDLED para indicar que nenhum processamento adicional é necessário.</span><span class="sxs-lookup"><span data-stu-id="bb400-117">Returns PSNRET\_MESSAGEHANDLED to indicate that no further processing is necessary.</span></span> <span data-ttu-id="bb400-118">Retorna PSNRET \_ NOERROR para solicitar o processamento normal.</span><span class="sxs-lookup"><span data-stu-id="bb400-118">Returns PSNRET\_NOERROR to request normal processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb400-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb400-119">Remarks</span></span>

<span data-ttu-id="bb400-120">Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor MSGRESULT DWL.</span><span class="sxs-lookup"><span data-stu-id="bb400-120">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value.</span></span> <span data-ttu-id="bb400-121">O procedimento da caixa de diálogo deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="bb400-121">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb400-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb400-122">Requirements</span></span>



| <span data-ttu-id="bb400-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb400-123">Requirement</span></span> | <span data-ttu-id="bb400-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bb400-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb400-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb400-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bb400-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb400-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bb400-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb400-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bb400-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb400-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb400-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb400-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb400-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb400-130"><dt>Prsht.h</dt></span></span> </dl> |



 

