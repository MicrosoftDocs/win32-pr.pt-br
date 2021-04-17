---
title: Mensagem de TVM_SETSCROLLTIME (commctrl. h)
description: Define o tempo máximo de rolagem para o controle de exibição em árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setrolation do TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- Controles de TVM_SETSCROLLTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753783"
---
# <a name="tvm_setscrolltime-message"></a><span data-ttu-id="ae6f9-105">TVM de \_ mensagem de AUTOrolagem</span><span class="sxs-lookup"><span data-stu-id="ae6f9-105">TVM\_SETSCROLLTIME message</span></span>

<span data-ttu-id="ae6f9-106">Define o tempo máximo de rolagem para o controle de exibição em árvore.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-106">Sets the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="ae6f9-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setrolation do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="ae6f9-107">You can send this message explicitly or by using the [**TreeView\_SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae6f9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae6f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae6f9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae6f9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae6f9-110">Novo tempo máximo de rolagem, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-110">New maximum scroll time, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="ae6f9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae6f9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ae6f9-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae6f9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae6f9-113">Return value</span></span>

<span data-ttu-id="ae6f9-114">Retorna o tempo máximo de rolagem anterior, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-114">Returns the previous maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae6f9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae6f9-115">Remarks</span></span>

<span data-ttu-id="ae6f9-116">O tempo máximo de rolagem é a quantidade mais longa de tempo que uma operação de rolagem pode tomar.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="ae6f9-117">A rolagem será ajustada para que a rolagem ocorra dentro do tempo máximo de rolagem.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-117">Scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="ae6f9-118">Uma operação de rolagem pode levar menos tempo do que o máximo.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6f9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae6f9-119">Requirements</span></span>



| <span data-ttu-id="ae6f9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6f9-120">Requirement</span></span> | <span data-ttu-id="ae6f9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ae6f9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6f9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6f9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6f9-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae6f9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae6f9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6f9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6f9-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae6f9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae6f9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae6f9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae6f9-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae6f9-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae6f9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae6f9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6f9-129">**TVM \_ GETrolatime**</span><span class="sxs-lookup"><span data-stu-id="ae6f9-129">**TVM\_GETSCROLLTIME**</span></span>](tvm-getscrolltime.md)
</dt> </dl>

 

 





