---
title: Mensagem de LVM_SETWORKAREAS (commctrl. h)
description: Define as áreas de trabalho dentro de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetWorkAreas do ListView.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- Controles de LVM_SETWORKAREAS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918960"
---
# <a name="lvm_setworkareas-message"></a><span data-ttu-id="b3745-105">\_Mensagem SETWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="b3745-105">LVM\_SETWORKAREAS message</span></span>

<span data-ttu-id="b3745-106">Define as áreas de trabalho dentro de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="b3745-106">Sets the working areas within a list-view control.</span></span> <span data-ttu-id="b3745-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetWorkAreas do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .</span><span class="sxs-lookup"><span data-stu-id="b3745-107">You can send this message explicitly or use the [**ListView\_SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3745-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3745-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3745-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3745-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3745-110">O número de estruturas na matriz em *lprc*.</span><span class="sxs-lookup"><span data-stu-id="b3745-110">The number of structures in the array at *lprc*.</span></span> <span data-ttu-id="b3745-111">O número máximo de áreas de trabalho permitidas é definido pelo \_ valor de WORKAREAS Max LV \_ .</span><span class="sxs-lookup"><span data-stu-id="b3745-111">The maximum number of working areas allowed is defined by the LV\_MAX\_WORKAREAS value.</span></span>

</dd> <dt>

<span data-ttu-id="b3745-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3745-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3745-113">Ponteiro para uma matriz de estruturas [**Rect**](/previous-versions//dd162897(v=vs.85)) que contêm as novas áreas de trabalho do controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="b3745-113">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that contain the new working areas of the list-view control.</span></span> <span data-ttu-id="b3745-114">Os valores nessas estruturas estão nas coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="b3745-114">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="b3745-115">Se esse parâmetro for **NULL**, a área de trabalho será definida como a área do cliente do controle.</span><span class="sxs-lookup"><span data-stu-id="b3745-115">If this parameter is **NULL**, the working area will be set to the client area of the control.</span></span> <span data-ttu-id="b3745-116">*wParam* especifica o número de estruturas nesta matriz.</span><span class="sxs-lookup"><span data-stu-id="b3745-116">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3745-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3745-117">Return value</span></span>

<span data-ttu-id="b3745-118">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="b3745-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3745-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3745-119">Requirements</span></span>



| <span data-ttu-id="b3745-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3745-120">Requirement</span></span> | <span data-ttu-id="b3745-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b3745-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3745-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3745-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3745-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3745-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3745-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3745-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3745-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b3745-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3745-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3745-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3745-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3745-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3745-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3745-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3745-129">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="b3745-129">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

