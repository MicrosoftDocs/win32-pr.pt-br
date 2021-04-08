---
title: Código de notificação de NM_CLICK (exibição de lista) (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário clica em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- NM_CLICK de código de notificação (exibição de lista) controles do Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d766767bfb742e5d7ea7c22a1266540a40d65b9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086545"
---
# <a name="nm_click-list-view-notification-code"></a><span data-ttu-id="8723d-105">\_Código de notificação de clique do nm (exibição de lista)</span><span class="sxs-lookup"><span data-stu-id="8723d-105">NM\_CLICK (list view) notification code</span></span>

<span data-ttu-id="8723d-106">Enviado por um controle de exibição de lista quando o usuário clica em um item com o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="8723d-106">Sent by a list-view control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="8723d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8723d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8723d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8723d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8723d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8723d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8723d-110">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="8723d-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="8723d-111">Ponteiro para uma estrutura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="8723d-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="8723d-112">Os membros **iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="8723d-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8723d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8723d-113">Return value</span></span>

<span data-ttu-id="8723d-114">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="8723d-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8723d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8723d-115">Remarks</span></span>

<span data-ttu-id="8723d-116">O membro **iItem** de *lParam* só será válido se o ícone ou rótulo de primeira coluna tiver sido clicado.</span><span class="sxs-lookup"><span data-stu-id="8723d-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="8723d-117">Para determinar qual item é selecionado quando um clique ocorre em outro lugar em uma linha, envie uma mensagem [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="8723d-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8723d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8723d-118">Requirements</span></span>



| <span data-ttu-id="8723d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8723d-119">Requirement</span></span> | <span data-ttu-id="8723d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8723d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8723d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8723d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8723d-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8723d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8723d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8723d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8723d-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8723d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8723d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8723d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8723d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8723d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





