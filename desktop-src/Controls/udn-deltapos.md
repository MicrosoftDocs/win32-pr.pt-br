---
title: UDN_DELTAPOS código de notificação (commctrl. h)
description: Enviado pelo sistema operacional para a janela pai de um controle de cima para baixo quando a posição do controle está prestes a ser alterada.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644695"
---
# <a name="udn_deltapos-notification-code"></a><span data-ttu-id="5b13d-104">Código de notificação do UDN \_ DELTAPOS</span><span class="sxs-lookup"><span data-stu-id="5b13d-104">UDN\_DELTAPOS notification code</span></span>

<span data-ttu-id="5b13d-105">Enviado pelo sistema operacional para a janela pai de um controle de cima para baixo quando a posição do controle está prestes a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="5b13d-105">Sent by the operating system to the parent window of an up-down control when the position of the control is about to change.</span></span> <span data-ttu-id="5b13d-106">Isso acontece quando o usuário solicita uma alteração no valor pressionando a seta para cima ou para baixo do controle.</span><span class="sxs-lookup"><span data-stu-id="5b13d-106">This happens when the user requests a change in the value by pressing the control's up or down arrow.</span></span> <span data-ttu-id="5b13d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5b13d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5b13d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b13d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b13d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b13d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b13d-110">Ponteiro para uma estrutura [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) que contém informações sobre a alteração de posição.</span><span class="sxs-lookup"><span data-stu-id="5b13d-110">Pointer to an [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) structure that contains information about the position change.</span></span> <span data-ttu-id="5b13d-111">O membro **IPOs** dessa estrutura contém a posição atual do controle.</span><span class="sxs-lookup"><span data-stu-id="5b13d-111">The **iPos** member of this structure contains the current position of the control.</span></span> <span data-ttu-id="5b13d-112">O membro **Idelta** da estrutura é um inteiro assinado que contém a alteração proposta na posição.</span><span class="sxs-lookup"><span data-stu-id="5b13d-112">The **iDelta** member of the structure is a signed integer that contains the proposed change in position.</span></span> <span data-ttu-id="5b13d-113">Se o usuário clicou no botão para cima, esse é um valor positivo.</span><span class="sxs-lookup"><span data-stu-id="5b13d-113">If the user has clicked the up button, this is a positive value.</span></span> <span data-ttu-id="5b13d-114">Se o usuário clicou no botão para baixo, esse é um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="5b13d-114">If the user has clicked the down button, this is a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b13d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b13d-115">Return value</span></span>

<span data-ttu-id="5b13d-116">Retorne diferente de zero para impedir a alteração na posição do controle ou zero para permitir a alteração.</span><span class="sxs-lookup"><span data-stu-id="5b13d-116">Return nonzero to prevent the change in the control's position, or zero to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b13d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b13d-117">Remarks</span></span>

<span data-ttu-id="5b13d-118">O \_ código de notificação UDN DELTAPOS é enviado antes da mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) ou do [**WM \_ HSCROLL**](wm-hscroll.md) , que, na verdade, altera a posição do controle.</span><span class="sxs-lookup"><span data-stu-id="5b13d-118">The UDN\_DELTAPOS notification code is sent before the [**WM\_VSCROLL**](wm-vscroll.md) or [**WM\_HSCROLL**](wm-hscroll.md) message, which actually changes the control's position.</span></span> <span data-ttu-id="5b13d-119">Isso permite que você examine, permita, modifique ou proíba a alteração.</span><span class="sxs-lookup"><span data-stu-id="5b13d-119">This lets you examine, allow, modify, or disallow the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b13d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b13d-120">Requirements</span></span>



| <span data-ttu-id="5b13d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b13d-121">Requirement</span></span> | <span data-ttu-id="5b13d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5b13d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b13d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b13d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5b13d-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b13d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b13d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b13d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5b13d-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b13d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b13d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b13d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b13d-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b13d-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b13d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b13d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b13d-130">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5b13d-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

