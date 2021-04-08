---
title: Mensagem de TBM_SETTICFREQ (commctrl. h)
description: Define a frequência de intervalo para marcas de escala em um TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- Controles de TBM_SETTICFREQ de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009118"
---
# <a name="tbm_setticfreq-message"></a><span data-ttu-id="f8a9b-104">\_Mensagem tbm SETTICFREQ</span><span class="sxs-lookup"><span data-stu-id="f8a9b-104">TBM\_SETTICFREQ message</span></span>

<span data-ttu-id="f8a9b-105">Define a frequência de intervalo para marcas de escala em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f8a9b-105">Sets the interval frequency for tick marks in a trackbar.</span></span> <span data-ttu-id="f8a9b-106">Por exemplo, se a frequência for definida como dois, uma marca de escala será exibida para todos os outros incrementos no intervalo do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f8a9b-106">For example, if the frequency is set to two, a tick mark is displayed for every other increment in the trackbar's range.</span></span> <span data-ttu-id="f8a9b-107">A configuração padrão para a frequência é uma; ou seja, cada incremento no intervalo é associado a uma marca de escala.</span><span class="sxs-lookup"><span data-stu-id="f8a9b-107">The default setting for the frequency is one; that is, every increment in the range is associated with a tick mark.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8a9b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8a9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a9b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8a9b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a9b-110">Frequência das marcas de escala.</span><span class="sxs-lookup"><span data-stu-id="f8a9b-110">Frequency of the tick marks.</span></span>

</dd> <dt>

<span data-ttu-id="f8a9b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8a9b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f8a9b-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f8a9b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a9b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8a9b-113">Return value</span></span>

<span data-ttu-id="f8a9b-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f8a9b-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a9b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8a9b-115">Remarks</span></span>

<span data-ttu-id="f8a9b-116">O TrackBar deve ter o estilo de [**\_ autotiques TBS**](trackbar-control-styles.md) para usar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="f8a9b-116">The trackbar must have the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) style to use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a9b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8a9b-117">Requirements</span></span>



| <span data-ttu-id="f8a9b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a9b-118">Requirement</span></span> | <span data-ttu-id="f8a9b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f8a9b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a9b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8a9b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a9b-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8a9b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8a9b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8a9b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a9b-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8a9b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8a9b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8a9b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a9b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a9b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





