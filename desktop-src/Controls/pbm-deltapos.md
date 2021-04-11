---
title: Mensagem de PBM_DELTAPOS (commctrl. h)
description: Avança a posição atual de uma barra de progresso por um incremento especificado e redesenha a barra para refletir a nova posição.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- Controles de PBM_DELTAPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009559"
---
# <a name="pbm_deltapos-message"></a><span data-ttu-id="044d5-104">Mensagem do DELTAPOS do PBM \_</span><span class="sxs-lookup"><span data-stu-id="044d5-104">PBM\_DELTAPOS message</span></span>

<span data-ttu-id="044d5-105">Avança a posição atual de uma barra de progresso por um incremento especificado e redesenha a barra para refletir a nova posição.</span><span class="sxs-lookup"><span data-stu-id="044d5-105">Advances the current position of a progress bar by a specified increment and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="044d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="044d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044d5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="044d5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="044d5-108">Valor para avançar a posição.</span><span class="sxs-lookup"><span data-stu-id="044d5-108">Amount to advance the position.</span></span>

</dd> <dt>

<span data-ttu-id="044d5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="044d5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="044d5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="044d5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="044d5-111">Return value</span></span>

<span data-ttu-id="044d5-112">Retorna a posição anterior.</span><span class="sxs-lookup"><span data-stu-id="044d5-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="044d5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="044d5-113">Remarks</span></span>

<span data-ttu-id="044d5-114">Se o incremento resultar em um valor fora do intervalo do controle, a posição será definida como o limite mais próximo.</span><span class="sxs-lookup"><span data-stu-id="044d5-114">If the increment results in a value outside the range of the control, the position is set to the nearest boundary.</span></span>

<span data-ttu-id="044d5-115">O comportamento dessa mensagem será indefinido se for enviado a um controle que tenha o estilo de [**\_ letreiro do PBS**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="044d5-115">The behavior of this message is undefined if it is sent to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="044d5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="044d5-116">Requirements</span></span>



| <span data-ttu-id="044d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="044d5-117">Requirement</span></span> | <span data-ttu-id="044d5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="044d5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="044d5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="044d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="044d5-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="044d5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="044d5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="044d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="044d5-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="044d5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="044d5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="044d5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="044d5-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="044d5-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





