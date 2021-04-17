---
title: Mensagem de MCM_SETMONTHDELTA (commctrl. h)
description: Define a taxa de rolagem para um controle de calendário mensal. A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- Controles de MCM_SETMONTHDELTA de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750939"
---
# <a name="mcm_setmonthdelta-message"></a><span data-ttu-id="0e483-106">\_Mensagem MCM SETMONTHDELTA</span><span class="sxs-lookup"><span data-stu-id="0e483-106">MCM\_SETMONTHDELTA message</span></span>

<span data-ttu-id="0e483-107">Define a taxa de rolagem para um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="0e483-107">Sets the scroll rate for a month calendar control.</span></span> <span data-ttu-id="0e483-108">A taxa de rolagem é o número de meses que o controle move sua exibição quando o usuário clica em um botão de rolagem.</span><span class="sxs-lookup"><span data-stu-id="0e483-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="0e483-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="0e483-109">You can send this message explicitly or by using the [**MonthCal\_SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e483-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e483-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e483-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e483-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e483-112">Valor que representa o número de meses a serem definidos como a taxa de rolagem do controle.</span><span class="sxs-lookup"><span data-stu-id="0e483-112">Value representing the number of months to be set as the control's scroll rate.</span></span> <span data-ttu-id="0e483-113">Se esse valor for zero, o Delta do mês será redefinido para o padrão, que é o número de meses exibidos no controle.</span><span class="sxs-lookup"><span data-stu-id="0e483-113">If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control.</span></span>

</dd> <dt>

<span data-ttu-id="0e483-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e483-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0e483-115">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0e483-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e483-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e483-116">Return value</span></span>

<span data-ttu-id="0e483-117">Retorna um valor INT que representa a taxa de rolagem anterior.</span><span class="sxs-lookup"><span data-stu-id="0e483-117">Returns an INT value that represents the previous scroll rate.</span></span> <span data-ttu-id="0e483-118">Se a taxa de rolagem não tiver sido definida anteriormente, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="0e483-118">If the scroll rate was not previously set, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e483-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e483-119">Remarks</span></span>

<span data-ttu-id="0e483-120">As teclas PAGE UP e PAGE DOWN, VK \_ anterior e VK \_ Next, alteram o mês selecionado em um, independentemente do número de meses exibidos ou do valor definido por **MCM \_ SETMONTHDELTA**.</span><span class="sxs-lookup"><span data-stu-id="0e483-120">The PAGE UP and PAGE DOWN keys, VK\_PRIOR and VK\_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by **MCM\_SETMONTHDELTA**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e483-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e483-121">Requirements</span></span>



| <span data-ttu-id="0e483-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e483-122">Requirement</span></span> | <span data-ttu-id="0e483-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0e483-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e483-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e483-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0e483-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e483-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e483-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e483-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0e483-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e483-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e483-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e483-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e483-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e483-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





