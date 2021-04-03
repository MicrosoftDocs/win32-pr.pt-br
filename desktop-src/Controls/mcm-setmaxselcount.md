---
title: Mensagem de MCM_SETMAXSELCOUNT (commctrl. h)
description: Define o número máximo de dias que podem ser selecionados em um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetMaxSelCount.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- Controles de MCM_SETMAXSELCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824757"
---
# <a name="mcm_setmaxselcount-message"></a><span data-ttu-id="d0011-105">\_Mensagem MCM SETMAXSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="d0011-105">MCM\_SETMAXSELCOUNT message</span></span>

<span data-ttu-id="d0011-106">Define o número máximo de dias que podem ser selecionados em um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="d0011-106">Sets the maximum number of days that can be selected in a month calendar control.</span></span> <span data-ttu-id="d0011-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="d0011-107">You can send this message explicitly or by using the [**MonthCal\_SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0011-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0011-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0011-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0011-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0011-110">Valor do tipo **int** que será definido para representar o número máximo de dias que podem ser selecionados.</span><span class="sxs-lookup"><span data-stu-id="d0011-110">Value of type **int** that will be set to represent the maximum number of days that can be selected.</span></span>

</dd> <dt>

<span data-ttu-id="d0011-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0011-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d0011-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d0011-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0011-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0011-113">Return value</span></span>

<span data-ttu-id="d0011-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="d0011-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="d0011-115">Esta mensagem falhará se for aplicada a um controle de calendário de mês que não usa o estilo de [**\_ multiseleção MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d0011-115">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0011-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0011-116">Requirements</span></span>



| <span data-ttu-id="d0011-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0011-117">Requirement</span></span> | <span data-ttu-id="d0011-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d0011-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0011-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0011-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0011-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0011-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0011-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0011-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0011-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0011-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0011-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0011-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0011-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0011-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





