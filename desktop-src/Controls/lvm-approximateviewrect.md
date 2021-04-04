---
title: Mensagem de LVM_APPROXIMATEVIEWRECT (commctrl. h)
description: Calcula a largura aproximada e a altura necessárias para exibir um determinado número de itens. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ApproximateViewRect do ListView.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- Controles de LVM_APPROXIMATEVIEWRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918000"
---
# <a name="lvm_approximateviewrect-message"></a><span data-ttu-id="e2f79-105">\_Mensagem APPROXIMATEVIEWRECT LVM</span><span class="sxs-lookup"><span data-stu-id="e2f79-105">LVM\_APPROXIMATEVIEWRECT message</span></span>

<span data-ttu-id="e2f79-106">Calcula a largura aproximada e a altura necessárias para exibir um determinado número de itens.</span><span class="sxs-lookup"><span data-stu-id="e2f79-106">Calculates the approximate width and height required to display a given number of items.</span></span> <span data-ttu-id="e2f79-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ ApproximateViewRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .</span><span class="sxs-lookup"><span data-stu-id="e2f79-107">You can send this message explicitly or use the [**ListView\_ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2f79-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2f79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f79-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2f79-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f79-110">O número de itens a serem exibidos no controle.</span><span class="sxs-lookup"><span data-stu-id="e2f79-110">The number of items to be displayed in the control.</span></span> <span data-ttu-id="e2f79-111">Se esse parâmetro for definido como-1, a mensagem usará o número total de itens no controle.</span><span class="sxs-lookup"><span data-stu-id="e2f79-111">If this parameter is set to -1, the message uses the total number of items in the control.</span></span>

</dd> <dt>

<span data-ttu-id="e2f79-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2f79-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f79-113">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é a dimensão x proposta do controle, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e2f79-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the proposed x-dimension of the control, in pixels.</span></span> <span data-ttu-id="e2f79-114">Esse parâmetro pode ser definido como-1 para permitir que a mensagem use o valor de largura atual.</span><span class="sxs-lookup"><span data-stu-id="e2f79-114">This parameter can be set to -1 to allow the message to use the current width value.</span></span>

<span data-ttu-id="e2f79-115">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é a dimensão y proposta do controle, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e2f79-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the proposed y-dimension of the control, in pixels.</span></span> <span data-ttu-id="e2f79-116">Esse parâmetro pode ser definido como-1 para permitir que a mensagem use o valor da altura atual.</span><span class="sxs-lookup"><span data-stu-id="e2f79-116">This parameter can be set to -1 to allow the message to use the current height value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f79-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2f79-117">Return value</span></span>

<span data-ttu-id="e2f79-118">Retorna um valor **DWORD** que contém a largura aproximada (no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) e a altura (no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) necessárias para exibir os itens, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e2f79-118">Returns a **DWORD** value that holds the approximate width (in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) and height (in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) needed to display the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f79-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2f79-119">Remarks</span></span>

<span data-ttu-id="e2f79-120">Definir o tamanho do controle de exibição de lista com base nas dimensões fornecidas por essa mensagem pode otimizar o redesenho e a redução da cintilação.</span><span class="sxs-lookup"><span data-stu-id="e2f79-120">Setting the size of the list-view control based on the dimensions provided by this message can optimize redraw and reduce flicker.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f79-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f79-121">Requirements</span></span>



| <span data-ttu-id="e2f79-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f79-122">Requirement</span></span> | <span data-ttu-id="e2f79-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e2f79-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f79-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2f79-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f79-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2f79-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2f79-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2f79-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f79-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2f79-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2f79-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2f79-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2f79-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f79-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

