---
title: Mensagem de LVM_GETWORKAREAS (commctrl. h)
description: Recupera as áreas de trabalho de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetWorkAreas do ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- Controles de LVM_GETWORKAREAS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455742"
---
# <a name="lvm_getworkareas-message"></a><span data-ttu-id="0ac47-105">\_Mensagem GETWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="0ac47-105">LVM\_GETWORKAREAS message</span></span>

<span data-ttu-id="0ac47-106">Recupera as áreas de trabalho de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="0ac47-106">Retrieves the working areas from a list-view control.</span></span> <span data-ttu-id="0ac47-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetWorkAreas do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .</span><span class="sxs-lookup"><span data-stu-id="0ac47-107">You can send this message explicitly or use the [**ListView\_GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ac47-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ac47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac47-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ac47-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ac47-110">O número de estruturas [**Rect**](/previous-versions//dd162897(v=vs.85)) na matriz em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="0ac47-110">The number of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures in the array at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="0ac47-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ac47-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ac47-112">Ponteiro para uma matriz de estruturas [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebem as áreas de trabalho atuais do controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="0ac47-112">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that receive the current working areas of the list-view control.</span></span> <span data-ttu-id="0ac47-113">Os valores nessas estruturas estão nas coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="0ac47-113">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="0ac47-114">*wParam* especifica o número de estruturas nesta matriz.</span><span class="sxs-lookup"><span data-stu-id="0ac47-114">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac47-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ac47-115">Return value</span></span>

<span data-ttu-id="0ac47-116">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="0ac47-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac47-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ac47-117">Requirements</span></span>



| <span data-ttu-id="0ac47-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac47-118">Requirement</span></span> | <span data-ttu-id="0ac47-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0ac47-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac47-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ac47-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac47-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ac47-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ac47-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ac47-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac47-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ac47-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ac47-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ac47-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ac47-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ac47-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac47-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ac47-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac47-127">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="0ac47-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

