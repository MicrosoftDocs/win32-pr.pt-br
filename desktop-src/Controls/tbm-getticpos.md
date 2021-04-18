---
title: Mensagem de TBM_GETTICPOS (commctrl. h)
description: Recupera a posição física atual de uma marca de escala em um TrackBar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- Controles de TBM_GETTICPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750300"
---
# <a name="tbm_getticpos-message"></a><span data-ttu-id="dd978-104">\_Mensagem tbm GETTICPOS</span><span class="sxs-lookup"><span data-stu-id="dd978-104">TBM\_GETTICPOS message</span></span>

<span data-ttu-id="dd978-105">Recupera a posição física atual de uma marca de escala em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="dd978-105">Retrieves the current physical position of a tick mark in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd978-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd978-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd978-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd978-108">Índice com base em zero que identifica uma marca de escala.</span><span class="sxs-lookup"><span data-stu-id="dd978-108">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="dd978-109">As posições da primeira e da última marca de escala não estão diretamente disponíveis por esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="dd978-109">The positions of the first and last tick marks are not directly available via this message.</span></span>

</dd> <dt>

<span data-ttu-id="dd978-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd978-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd978-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dd978-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd978-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd978-112">Return value</span></span>

<span data-ttu-id="dd978-113">Retorna a distância, em coordenadas do cliente, do lado esquerdo ou superior da área do cliente do TrackBar para a marca de escala especificada.</span><span class="sxs-lookup"><span data-stu-id="dd978-113">Returns the distance, in client coordinates, from the left or top of the trackbar's client area to the specified tick mark.</span></span> <span data-ttu-id="dd978-114">O valor de retorno é a coordenada x da marca de escala para uma TrackBar horizontal ou a coordenada y para um TrackBar vertical.</span><span class="sxs-lookup"><span data-stu-id="dd978-114">The return value is the x-coordinate of the tick mark for a horizontal trackbar or the y-coordinate for a vertical trackbar.</span></span> <span data-ttu-id="dd978-115">Se *wParam* não for um índice válido, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="dd978-115">If *wParam* is not a valid index, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd978-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd978-116">Remarks</span></span>

<span data-ttu-id="dd978-117">Como a primeira e a última marca de escala não estão disponíveis por essa mensagem, os índices válidos são deslocados da posição de tique na TrackBar.</span><span class="sxs-lookup"><span data-stu-id="dd978-117">Because the first and last tick marks are not available through this message, valid indexes are offset from their tick position on the trackbar.</span></span> <span data-ttu-id="dd978-118">Se a diferença entre [**tbm \_ GETRANGEMIN**](tbm-getrangemin.md) e [**tbm \_ GETRANGEMAX**](tbm-getrangemax.md) for menor que dois, não haverá nenhum índice válido e essa mensagem falhará.</span><span class="sxs-lookup"><span data-stu-id="dd978-118">If the difference between [**TBM\_GETRANGEMIN**](tbm-getrangemin.md) and [**TBM\_GETRANGEMAX**](tbm-getrangemax.md) is less than two, then there is no valid index and this message will fail.</span></span>

<span data-ttu-id="dd978-119">O seguinte ilustra a relação entre os tiques em um TrackBar, os tiques disponíveis por essa mensagem e seus índices com base em zero.</span><span class="sxs-lookup"><span data-stu-id="dd978-119">The following illustrates the relation between the ticks on a trackbar, the ticks available through this message, and their zero-based indexes.</span></span>

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a><span data-ttu-id="dd978-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd978-120">Requirements</span></span>



| <span data-ttu-id="dd978-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd978-121">Requirement</span></span> | <span data-ttu-id="dd978-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dd978-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd978-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd978-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dd978-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd978-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd978-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd978-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dd978-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd978-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd978-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd978-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd978-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd978-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





