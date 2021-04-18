---
title: Código de notificação BCN_DROPDOWN (WinUser. h)
description: Enviado quando o usuário clica em uma seta suspensa em um botão. A janela pai do controle recebe esse código de notificação na forma de uma mensagem de \_ notificação do WM.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756428"
---
# <a name="bcn_dropdown-notification-code"></a><span data-ttu-id="e3e02-105">\_Código de notificação da lista suspensa BCN</span><span class="sxs-lookup"><span data-stu-id="e3e02-105">BCN\_DROPDOWN notification code</span></span>

<span data-ttu-id="e3e02-106">Enviado quando o usuário clica em uma seta suspensa em um botão.</span><span class="sxs-lookup"><span data-stu-id="e3e02-106">Sent when the user clicks a drop down arrow on a button.</span></span> <span data-ttu-id="e3e02-107">A janela pai do controle recebe esse código de notificação na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e3e02-107">The parent window of the control receives this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e3e02-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3e02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e02-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e3e02-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e02-110">Um ponteiro para uma estrutura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="e3e02-110">A pointer to a [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="e3e02-111">O membro **rcButton** é definido para descrever a área suspensa.</span><span class="sxs-lookup"><span data-stu-id="e3e02-111">The **rcButton** member is set to describe the drop-down area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e02-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3e02-112">Return value</span></span>

<span data-ttu-id="e3e02-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e3e02-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3e02-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3e02-114">Remarks</span></span>

<span data-ttu-id="e3e02-115">O receptor de notificação converte **lParam** para recuperar a estrutura [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) .</span><span class="sxs-lookup"><span data-stu-id="e3e02-115">The notification receiver casts **LPARAM** to retrieve the [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) structure.</span></span> <span data-ttu-id="e3e02-116">**WParam** contém a ID do controle que envia essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="e3e02-116">**WPARAM** contains the ID of the control that sends this message.</span></span> <span data-ttu-id="e3e02-117">O controle de botão deve ter um estilo de botão suspenso.</span><span class="sxs-lookup"><span data-stu-id="e3e02-117">The button control must have a drop-down button style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e02-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3e02-118">Requirements</span></span>



| <span data-ttu-id="e3e02-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3e02-119">Requirement</span></span> | <span data-ttu-id="e3e02-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e3e02-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e02-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3e02-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3e02-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3e02-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3e02-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3e02-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3e02-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3e02-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3e02-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3e02-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3e02-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3e02-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





