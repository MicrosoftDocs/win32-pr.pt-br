---
title: Mensagem de LVM_GETCOUNTPERPAGE (commctrl. h)
description: Calcula o número de itens que podem se ajustar verticalmente na área visível de um controle de exibição de lista no modo de exibição de lista ou de relatório. Somente os itens totalmente visíveis são contados. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetCountPerPage do ListView.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- Controles de LVM_GETCOUNTPERPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008866"
---
# <a name="lvm_getcountperpage-message"></a><span data-ttu-id="f7e6d-106">\_Mensagem GETCOUNTPERPAGE LVM</span><span class="sxs-lookup"><span data-stu-id="f7e6d-106">LVM\_GETCOUNTPERPAGE message</span></span>

<span data-ttu-id="f7e6d-107">Calcula o número de itens que podem se ajustar verticalmente na área visível de um controle de exibição de lista no modo de exibição de lista ou de relatório.</span><span class="sxs-lookup"><span data-stu-id="f7e6d-107">Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view.</span></span> <span data-ttu-id="f7e6d-108">Somente os itens totalmente visíveis são contados.</span><span class="sxs-lookup"><span data-stu-id="f7e6d-108">Only fully visible items are counted.</span></span> <span data-ttu-id="f7e6d-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetCountPerPage do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) .</span><span class="sxs-lookup"><span data-stu-id="f7e6d-109">You can send this message explicitly or by using the [**ListView\_GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7e6d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7e6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7e6d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7e6d-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f7e6d-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f7e6d-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f7e6d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7e6d-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f7e6d-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f7e6d-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7e6d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7e6d-115">Return value</span></span>

<span data-ttu-id="f7e6d-116">Retorna o número de itens totalmente visíveis se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f7e6d-116">Returns the number of fully visible items if successful.</span></span> <span data-ttu-id="f7e6d-117">Se a exibição atual for ícone ou exibição de ícone pequeno, o valor de retorno será o número total de itens no controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="f7e6d-117">If the current view is icon or small icon view, the return value is the total number of items in the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e6d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7e6d-118">Requirements</span></span>



| <span data-ttu-id="f7e6d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7e6d-119">Requirement</span></span> | <span data-ttu-id="f7e6d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f7e6d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e6d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7e6d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e6d-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7e6d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7e6d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7e6d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e6d-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f7e6d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7e6d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f7e6d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7e6d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7e6d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





