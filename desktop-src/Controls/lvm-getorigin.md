---
title: Mensagem de LVM_GETORIGIN (commctrl. h)
description: Recupera a origem da exibição atual para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro getorigin de ListView.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- Controles de LVM_GETORIGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086161"
---
# <a name="lvm_getorigin-message"></a><span data-ttu-id="e8d77-105">\_Mensagem de GETorigin do LVM</span><span class="sxs-lookup"><span data-stu-id="e8d77-105">LVM\_GETORIGIN message</span></span>

<span data-ttu-id="e8d77-106">Recupera a origem da exibição atual para um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="e8d77-106">Retrieves the current view origin for a list-view control.</span></span> <span data-ttu-id="e8d77-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ getorigin de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) .</span><span class="sxs-lookup"><span data-stu-id="e8d77-107">You can send this message explicitly or by using the [**ListView\_GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8d77-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8d77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8d77-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8d77-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e8d77-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e8d77-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e8d77-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8d77-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8d77-112">Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que recebe a origem da exibição.</span><span class="sxs-lookup"><span data-stu-id="e8d77-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the view origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8d77-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8d77-113">Return value</span></span>

<span data-ttu-id="e8d77-114">Retornará **true** se for bem-sucedido ou **false** se a exibição atual for lista ou relatório.</span><span class="sxs-lookup"><span data-stu-id="e8d77-114">Returns **TRUE** if successful, or **FALSE** if the current view is list or report view.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8d77-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8d77-115">Requirements</span></span>



| <span data-ttu-id="e8d77-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8d77-116">Requirement</span></span> | <span data-ttu-id="e8d77-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e8d77-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d77-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8d77-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d77-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8d77-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8d77-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8d77-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d77-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8d77-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8d77-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8d77-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8d77-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8d77-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

