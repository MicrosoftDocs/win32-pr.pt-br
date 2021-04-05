---
title: Mensagem de LVM_GETNUMBEROFWORKAREAS (commctrl. h)
description: Recupera o número de áreas de trabalho em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetNumberOfWorkAreas do ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- Controles de LVM_GETNUMBEROFWORKAREAS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918968"
---
# <a name="lvm_getnumberofworkareas-message"></a><span data-ttu-id="d2068-105">\_Mensagem GETNUMBEROFWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="d2068-105">LVM\_GETNUMBEROFWORKAREAS message</span></span>

<span data-ttu-id="d2068-106">Recupera o número de áreas de trabalho em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="d2068-106">Retrieves the number of working areas in a list-view control.</span></span> <span data-ttu-id="d2068-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetNumberOfWorkAreas do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .</span><span class="sxs-lookup"><span data-stu-id="d2068-107">You can send this message explicitly or use the [**ListView\_GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2068-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2068-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2068-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2068-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d2068-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d2068-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d2068-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2068-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2068-112">Ponteiro para um valor UINT que recebe o número de áreas de trabalho no controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="d2068-112">Pointer to a UINT value that receives the number of working areas in the list-view control.</span></span> <span data-ttu-id="d2068-113">Se zero for colocado nessa variável, nenhuma área de trabalho estará definida no momento.</span><span class="sxs-lookup"><span data-stu-id="d2068-113">If zero is placed in this variable, then no working areas are currently set.</span></span> <span data-ttu-id="d2068-114">Esse valor não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d2068-114">This value cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2068-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2068-115">Return value</span></span>

<span data-ttu-id="d2068-116">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="d2068-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2068-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2068-117">Requirements</span></span>



| <span data-ttu-id="d2068-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2068-118">Requirement</span></span> | <span data-ttu-id="d2068-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d2068-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2068-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2068-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2068-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2068-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2068-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2068-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2068-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2068-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2068-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2068-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2068-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2068-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2068-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2068-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2068-127">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="d2068-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





