---
title: PSN_QUERYINITIALFOCUS código de notificação (Prsht. h)
description: Enviado por uma folha de propriedades para fornecer uma página de folha de propriedades a oportunidade de especificar qual controle de caixa de diálogo deve receber o foco inicial. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085210"
---
# <a name="psn_queryinitialfocus-notification-code"></a><span data-ttu-id="3bbc2-105">Código de notificação do PSN \_ QUERYINITIALFOCUS</span><span class="sxs-lookup"><span data-stu-id="3bbc2-105">PSN\_QUERYINITIALFOCUS notification code</span></span>

<span data-ttu-id="3bbc2-106">Enviado por uma folha de propriedades para fornecer uma página de folha de propriedades a oportunidade de especificar qual controle de caixa de diálogo deve receber o foco inicial.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-106">Sent by a property sheet to provide a property sheet page an opportunity to specify which dialog box control should receive the initial focus.</span></span> <span data-ttu-id="3bbc2-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3bbc2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3bbc2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bbc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bbc2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3bbc2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bbc2-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) .</span><span class="sxs-lookup"><span data-stu-id="3bbc2-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure.</span></span> <span data-ttu-id="3bbc2-111">Converta o membro **lParam** dessa estrutura em um tipo **HWND** para recuperar o identificador do controle que receberá o foco por padrão.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-111">Cast the **lParam** member of this structure to an **HWND** type, to retrieve the handle of the control that will be given focus by default.</span></span> <span data-ttu-id="3bbc2-112">A estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-112">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bbc2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bbc2-113">Return value</span></span>

<span data-ttu-id="3bbc2-114">Para especificar qual controle deve receber o foco, retorne o identificador do controle.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-114">To specify which control should receive focus, return the control's handle.</span></span> <span data-ttu-id="3bbc2-115">Caso contrário, retornará zero e o foco vai para o controle padrão.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-115">Otherwise, return zero and focus will go to the default control.</span></span> <span data-ttu-id="3bbc2-116">Para definir o valor de retorno, o procedimento da caixa de diálogo deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com um valor de **\_ MSGRESULT DWL** e retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-116">To set the return value, the dialog box procedure must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a **DWL\_MSGRESULT** value and return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bbc2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bbc2-117">Remarks</span></span>

<span data-ttu-id="3bbc2-118">Um aplicativo não deve chamar a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) ao manipular esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-118">An application must not call the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function while handling this notification code.</span></span> <span data-ttu-id="3bbc2-119">Retornar o identificador do controle que deve receber o foco e o gerente da folha de propriedades tratará da alteração de foco.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-119">Return the handle of the control that should receive focus, and the property sheet manager will handle the focus change.</span></span>

<span data-ttu-id="3bbc2-120">O \_ código de notificação PSN QUERYINITIALFOCUS não será enviado se o gerente da folha de propriedades determinar que nenhum controle na página deve receber o foco.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-120">The PSN\_QUERYINITIALFOCUS notification code is not sent if the property sheet manager determines that no control on the page should receive focus.</span></span>

<span data-ttu-id="3bbc2-121">Este fragmento de código implementa um manipulador simples para PSN \_ QUERYINITIALFOCUS.</span><span class="sxs-lookup"><span data-stu-id="3bbc2-121">This code fragment implements a simple handler for PSN\_QUERYINITIALFOCUS.</span></span> <span data-ttu-id="3bbc2-122">Ele solicita que o foco inicial seja fornecido ao controle de local **( \_ localização da IDC**).</span><span class="sxs-lookup"><span data-stu-id="3bbc2-122">It requests that initial focus be given to the Location control (**IDC\_LOCATION**).</span></span>

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> <span data-ttu-id="3bbc2-123">Não há suporte para este código de notificação ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="3bbc2-123">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3bbc2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bbc2-124">Requirements</span></span>



| <span data-ttu-id="3bbc2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bbc2-125">Requirement</span></span> | <span data-ttu-id="3bbc2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3bbc2-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbc2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bbc2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3bbc2-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3bbc2-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3bbc2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bbc2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3bbc2-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3bbc2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3bbc2-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bbc2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bbc2-132"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bbc2-132"><dt>Prsht.h</dt></span></span> </dl> |



 

