---
title: Mensagem de LVM_GETHOVERTIME (commctrl. h)
description: Recupera a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Getfocalizetime de ListView.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- Controles de LVM_GETHOVERTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455432"
---
# <a name="lvm_gethovertime-message"></a><span data-ttu-id="2102d-105">Mensagem do LVM \_ GETfocalizetime</span><span class="sxs-lookup"><span data-stu-id="2102d-105">LVM\_GETHOVERTIME message</span></span>

<span data-ttu-id="2102d-106">Recupera a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="2102d-106">Retrieves the amount of time that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="2102d-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ getfocalizetime de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .</span><span class="sxs-lookup"><span data-stu-id="2102d-107">You can send this message explicitly or use the [**ListView\_GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2102d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2102d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2102d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2102d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2102d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2102d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2102d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2102d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2102d-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2102d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2102d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2102d-113">Return value</span></span>

<span data-ttu-id="2102d-114">Retorna o período de tempo, em milissegundos, que o cursor do mouse deve passar sobre um item antes de ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="2102d-114">Returns the amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="2102d-115">Se o valor de retorno for (**DWORD**)-1, o tempo de foco será o tempo de focalização padrão.</span><span class="sxs-lookup"><span data-stu-id="2102d-115">If the return value is (**DWORD**)-1, then the hover time is the default hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="2102d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2102d-116">Remarks</span></span>

<span data-ttu-id="2102d-117">O tempo de foco afeta apenas os controles de exibição de lista que têm o estilo de exibição de lista estendida [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2102d-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2102d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2102d-118">Requirements</span></span>



| <span data-ttu-id="2102d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2102d-119">Requirement</span></span> | <span data-ttu-id="2102d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2102d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2102d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2102d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2102d-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2102d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2102d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2102d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2102d-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2102d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2102d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2102d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2102d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2102d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





