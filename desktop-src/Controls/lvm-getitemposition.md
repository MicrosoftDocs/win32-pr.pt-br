---
title: Mensagem de LVM_GETITEMPOSITION (commctrl. h)
description: Recupera a posição de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemPosition do ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- Controles de LVM_GETITEMPOSITION de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824672"
---
# <a name="lvm_getitemposition-message"></a><span data-ttu-id="9d85c-105">\_Mensagem GETITEMPOSITION LVM</span><span class="sxs-lookup"><span data-stu-id="9d85c-105">LVM\_GETITEMPOSITION message</span></span>

<span data-ttu-id="9d85c-106">Recupera a posição de um item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="9d85c-106">Retrieves the position of a list-view item.</span></span> <span data-ttu-id="9d85c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemPosition do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .</span><span class="sxs-lookup"><span data-stu-id="9d85c-107">You can send this message explicitly or by using the [**ListView\_GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d85c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d85c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d85c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d85c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d85c-110">Índice do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="9d85c-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="9d85c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d85c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d85c-112">Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que recebe a posição do canto superior esquerdo do item, em coordenadas de exibição.</span><span class="sxs-lookup"><span data-stu-id="9d85c-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d85c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d85c-113">Return value</span></span>

<span data-ttu-id="9d85c-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9d85c-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d85c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d85c-115">Requirements</span></span>



| <span data-ttu-id="9d85c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d85c-116">Requirement</span></span> | <span data-ttu-id="9d85c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9d85c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d85c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d85c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9d85c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d85c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d85c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d85c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9d85c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9d85c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d85c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d85c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d85c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d85c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

