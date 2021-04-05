---
title: Mensagem de LVM_SETHOVERTIME (commctrl. h)
description: Define a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Setfocalizetime do ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- Controles de LVM_SETHOVERTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085166"
---
# <a name="lvm_sethovertime-message"></a><span data-ttu-id="ea331-105">Mensagem do LVM \_ SETfocalizetime</span><span class="sxs-lookup"><span data-stu-id="ea331-105">LVM\_SETHOVERTIME message</span></span>

<span data-ttu-id="ea331-106">Define a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="ea331-106">Sets the amount of time which the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="ea331-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ setfocalizetime do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .</span><span class="sxs-lookup"><span data-stu-id="ea331-107">You can send this message explicitly or use the [**ListView\_SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea331-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea331-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea331-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea331-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ea331-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ea331-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ea331-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea331-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea331-112">A nova quantidade de tempo, em milissegundos, que o cursor do mouse deve passar sobre um item antes de ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="ea331-112">The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="ea331-113">Se esse valor for (**DWORD**)-1, o tempo de foco será definido como o tempo de foco padrão.</span><span class="sxs-lookup"><span data-stu-id="ea331-113">If this value is (**DWORD**)-1, then the hover time is set to the default hover time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea331-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea331-114">Return value</span></span>

<span data-ttu-id="ea331-115">Retorna o tempo de focalização anterior.</span><span class="sxs-lookup"><span data-stu-id="ea331-115">Returns the previous hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea331-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea331-116">Remarks</span></span>

<span data-ttu-id="ea331-117">O tempo de foco afeta apenas os controles de exibição de lista que têm o estilo de exibição de lista estendida [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ea331-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea331-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea331-118">Requirements</span></span>



| <span data-ttu-id="ea331-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea331-119">Requirement</span></span> | <span data-ttu-id="ea331-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ea331-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea331-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea331-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea331-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea331-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea331-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea331-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea331-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea331-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea331-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea331-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea331-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea331-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





