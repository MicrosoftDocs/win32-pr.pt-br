---
title: Código de notificação de NM_RCLICK (exibição de lista) (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário clica em um item com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: dc7f97b3-4aec-4a8f-a87c-62cef5ba4c40
keywords:
- NM_RCLICK de código de notificação (exibição de lista) controles do Windows
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01c21f1b1e869a909dd41dcfce693bf084f2fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085634"
---
# <a name="nm_rclick-list-view-notification-code"></a><span data-ttu-id="f4999-105">\_Código de notificação nm RCLICK (exibição de lista)</span><span class="sxs-lookup"><span data-stu-id="f4999-105">NM\_RCLICK (list view) notification code</span></span>

<span data-ttu-id="f4999-106">Enviado por um controle de exibição de lista quando o usuário clica em um item com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="f4999-106">Sent by a list-view control when the user clicks an item with the right mouse button.</span></span> <span data-ttu-id="f4999-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f4999-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f4999-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4999-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4999-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4999-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4999-110">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="f4999-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="f4999-111">Ponteiro para uma estrutura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="f4999-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="f4999-112">Os membros **iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="f4999-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4999-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4999-113">Return value</span></span>

<span data-ttu-id="f4999-114">Retornar zero para não permitir o processamento padrão ou zero para permitir o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="f4999-114">Return nonzero to not allow the default processing, or zero to allow the default processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4999-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4999-115">Remarks</span></span>

<span data-ttu-id="f4999-116">O membro **iItem** de *lParam* só será válido se o ícone ou rótulo de primeira coluna tiver sido clicado.</span><span class="sxs-lookup"><span data-stu-id="f4999-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="f4999-117">Para determinar qual item é selecionado quando um clique ocorre em outro lugar em uma linha, envie uma mensagem [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="f4999-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4999-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4999-118">Requirements</span></span>



| <span data-ttu-id="f4999-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4999-119">Requirement</span></span> | <span data-ttu-id="f4999-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f4999-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4999-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4999-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4999-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4999-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4999-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4999-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4999-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4999-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4999-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4999-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4999-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4999-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





