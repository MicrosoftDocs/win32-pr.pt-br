---
title: Código de notificação de NM_RDBLCLK (exibição de lista) (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário clica duas vezes em um item com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK de código de notificação (exibição de lista) controles do Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41832b228fe40b212c0aba809b15022c6f7b39ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919237"
---
# <a name="nm_rdblclk-list-view-notification-code"></a><span data-ttu-id="f49cd-105">\_Código de notificação nm RDBLCLK (exibição de lista)</span><span class="sxs-lookup"><span data-stu-id="f49cd-105">NM\_RDBLCLK (list view) notification code</span></span>

<span data-ttu-id="f49cd-106">Enviado por um controle de exibição de lista quando o usuário clica duas vezes em um item com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="f49cd-106">Sent by a list-view control when the user double-clicks an item with the right mouse button.</span></span> <span data-ttu-id="f49cd-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f49cd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f49cd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f49cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f49cd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f49cd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f49cd-110">[Versão 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="f49cd-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="f49cd-111">Ponteiro para uma estrutura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações adicionais sobre esta notificação.</span><span class="sxs-lookup"><span data-stu-id="f49cd-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="f49cd-112">Os membros **iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="f49cd-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f49cd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f49cd-113">Return value</span></span>

<span data-ttu-id="f49cd-114">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="f49cd-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f49cd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f49cd-115">Remarks</span></span>

<span data-ttu-id="f49cd-116">O membro **iItem** de *lParam* será válido somente se o ícone ou rótulo de primeira coluna tiver sido clicado.</span><span class="sxs-lookup"><span data-stu-id="f49cd-116">The **iItem** member of *lParam* is valid only if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="f49cd-117">Para determinar qual item é selecionado quando um clique ocorre em outro lugar em uma linha, envie uma mensagem [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="f49cd-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f49cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f49cd-118">Requirements</span></span>



| <span data-ttu-id="f49cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f49cd-119">Requirement</span></span> | <span data-ttu-id="f49cd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f49cd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f49cd-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f49cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f49cd-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f49cd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f49cd-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f49cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f49cd-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f49cd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f49cd-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f49cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f49cd-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f49cd-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





