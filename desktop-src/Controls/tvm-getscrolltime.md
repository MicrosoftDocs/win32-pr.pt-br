---
title: Mensagem de TVM_GETSCROLLTIME (commctrl. h)
description: Recupera o tempo máximo de rolagem para o controle de exibição em árvore. Você pode enviar essa mensagem explicitamente ou usando a macro do TreeView \_ getrolation.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- Controles de TVM_GETSCROLLTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085328"
---
# <a name="tvm_getscrolltime-message"></a><span data-ttu-id="eb865-105">\_Mensagem TVM GETscrolltime</span><span class="sxs-lookup"><span data-stu-id="eb865-105">TVM\_GETSCROLLTIME message</span></span>

<span data-ttu-id="eb865-106">Recupera o tempo máximo de rolagem para o controle de exibição em árvore.</span><span class="sxs-lookup"><span data-stu-id="eb865-106">Retrieves the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="eb865-107">Você pode enviar essa mensagem explicitamente ou usando a macro do [**TreeView \_ getrolation**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="eb865-107">You can send this message explicitly or by using the [**TreeView\_GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb865-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb865-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb865-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb865-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eb865-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="eb865-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eb865-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb865-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eb865-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="eb865-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb865-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb865-113">Return value</span></span>

<span data-ttu-id="eb865-114">Retorna o tempo máximo de rolagem, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="eb865-114">Returns the maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb865-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb865-115">Remarks</span></span>

<span data-ttu-id="eb865-116">O tempo máximo de rolagem é a quantidade mais longa de tempo que uma operação de rolagem pode tomar.</span><span class="sxs-lookup"><span data-stu-id="eb865-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="eb865-117">A rolagem será ajustada para que a rolagem ocorra dentro do tempo máximo de rolagem.</span><span class="sxs-lookup"><span data-stu-id="eb865-117">The scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="eb865-118">Uma operação de rolagem pode levar menos tempo do que o máximo.</span><span class="sxs-lookup"><span data-stu-id="eb865-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb865-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb865-119">Requirements</span></span>



| <span data-ttu-id="eb865-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb865-120">Requirement</span></span> | <span data-ttu-id="eb865-121">Valor</span><span class="sxs-lookup"><span data-stu-id="eb865-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb865-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb865-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eb865-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb865-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb865-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb865-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eb865-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb865-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb865-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb865-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb865-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb865-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb865-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb865-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb865-129">**TVM \_ SETrolatime**</span><span class="sxs-lookup"><span data-stu-id="eb865-129">**TVM\_SETSCROLLTIME**</span></span>](tvm-setscrolltime.md)
</dt> </dl>

 

 





