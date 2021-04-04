---
title: Mensagem de HDM_CLEARFILTER (commctrl. h)
description: Limpa o filtro de um determinado controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ClearFilter do cabeçalho.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- Controles de HDM_CLEARFILTER de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085826"
---
# <a name="hdm_clearfilter-message"></a><span data-ttu-id="3df9c-105">\_Mensagem HDM CLEARFILTER</span><span class="sxs-lookup"><span data-stu-id="3df9c-105">HDM\_CLEARFILTER message</span></span>

<span data-ttu-id="3df9c-106">Limpa o filtro de um determinado controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="3df9c-106">Clears the filter for a given header control.</span></span> <span data-ttu-id="3df9c-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ ClearFilter do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .</span><span class="sxs-lookup"><span data-stu-id="3df9c-107">You can send this message explicitly or use the [**Header\_ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3df9c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3df9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df9c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3df9c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3df9c-110">Um valor de coluna que indica qual filtro deve ser limpo.</span><span class="sxs-lookup"><span data-stu-id="3df9c-110">A column value indicating which filter to clear.</span></span>

</dd> <dt>

<span data-ttu-id="3df9c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3df9c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3df9c-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3df9c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df9c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3df9c-113">Return value</span></span>

<span data-ttu-id="3df9c-114">Retorna um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="3df9c-114">Returns an integer.</span></span> <span data-ttu-id="3df9c-115">O **LRESULT** é convertido em um inteiro que indica **true**(1) ou **false**(0).</span><span class="sxs-lookup"><span data-stu-id="3df9c-115">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="remarks"></a><span data-ttu-id="3df9c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3df9c-116">Remarks</span></span>

<span data-ttu-id="3df9c-117">Se o valor da coluna for especificado como-1, todos os filtros serão limpos e a notificação [HDN \_ FILTERCHANGE](hdn-filterchange.md) será enviada apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="3df9c-117">If the column value is specified as -1, all the filters are cleared, and the [HDN\_FILTERCHANGE](hdn-filterchange.md) notification is sent only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="3df9c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3df9c-118">Requirements</span></span>



| <span data-ttu-id="3df9c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3df9c-119">Requirement</span></span> | <span data-ttu-id="3df9c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3df9c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3df9c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3df9c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3df9c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3df9c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3df9c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3df9c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3df9c-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3df9c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3df9c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3df9c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df9c-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3df9c-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3df9c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3df9c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df9c-128">**ClearAllFilters de cabeçalho \_**</span><span class="sxs-lookup"><span data-stu-id="3df9c-128">**Header\_ClearAllFilters**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





