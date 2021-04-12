---
title: Mensagem de TBM_GETTIC (commctrl. h)
description: Recupera a posição lógica de uma marca de escala em um TrackBar. A posição lógica pode ser qualquer um dos valores inteiros na faixa de TrackBar de mínimo para máximo de posições do controle deslizante.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- Controles de TBM_GETTIC de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455173"
---
# <a name="tbm_gettic-message"></a><span data-ttu-id="6129a-105">\_Mensagem tbm GETTIC</span><span class="sxs-lookup"><span data-stu-id="6129a-105">TBM\_GETTIC message</span></span>

<span data-ttu-id="6129a-106">Recupera a posição lógica de uma marca de escala em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6129a-106">Retrieves the logical position of a tick mark in a trackbar.</span></span> <span data-ttu-id="6129a-107">A posição lógica pode ser qualquer um dos valores inteiros na faixa de TrackBar de mínimo para máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="6129a-107">The logical position can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="6129a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6129a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6129a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6129a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6129a-110">Índice com base em zero que identifica uma marca de escala.</span><span class="sxs-lookup"><span data-stu-id="6129a-110">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="6129a-111">Os índices válidos estão no intervalo de zero a dois menores que a contagem de tiques retornada pela mensagem [**tbm \_ GETNUMTICS**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="6129a-111">Valid indexes are in the range from zero to two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6129a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6129a-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6129a-113">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6129a-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6129a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6129a-114">Return value</span></span>

<span data-ttu-id="6129a-115">Retorna a posição lógica da marca de escala especificada, ou-1 se *wParam* não especificar um índice válido.</span><span class="sxs-lookup"><span data-stu-id="6129a-115">Returns the logical position of the specified tick mark, or -1 if *wParam* does not specify a valid index.</span></span>

## <a name="requirements"></a><span data-ttu-id="6129a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6129a-116">Requirements</span></span>



| <span data-ttu-id="6129a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6129a-117">Requirement</span></span> | <span data-ttu-id="6129a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6129a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6129a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6129a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6129a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6129a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6129a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6129a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6129a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6129a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6129a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6129a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6129a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6129a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





