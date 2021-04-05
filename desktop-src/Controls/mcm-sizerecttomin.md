---
title: Mensagem de MCM_SIZERECTTOMIN (commctrl. h)
description: Calcula quantos calendários serão ajustados no retângulo fornecido e, em seguida, retorna o tamanho mínimo que um retângulo precisa para ajustar esse número de calendários. Você pode enviar essa mensagem explicitamente ou usando a macro calendário mensal \_ SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- Controles de MCM_SIZERECTTOMIN de mensagens do Windows
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086323"
---
# <a name="mcm_sizerecttomin-message"></a><span data-ttu-id="16b1c-105">\_Mensagem MCM SIZERECTTOMIN</span><span class="sxs-lookup"><span data-stu-id="16b1c-105">MCM\_SIZERECTTOMIN message</span></span>

<span data-ttu-id="16b1c-106">Calcula quantos calendários serão ajustados no retângulo fornecido e, em seguida, retorna o tamanho mínimo que um retângulo precisa para ajustar esse número de calendários.</span><span class="sxs-lookup"><span data-stu-id="16b1c-106">Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars.</span></span> <span data-ttu-id="16b1c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**calendário mensal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .</span><span class="sxs-lookup"><span data-stu-id="16b1c-107">You can send this message explicitly or by using the [**MonthCal\_SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="16b1c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16b1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b1c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16b1c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16b1c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="16b1c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="16b1c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16b1c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16b1c-112">Na entrada, contém um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que descreve uma região maior ou igual ao tamanho necessário para se ajustar ao número desejado de calendários.</span><span class="sxs-lookup"><span data-stu-id="16b1c-112">On entry, contains a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that describes a region that is greater than or equal to the size necessary to fit the desired number of calendars.</span></span> <span data-ttu-id="16b1c-113">Quando essa função retorna, contém a estrutura de **Rect** mínima que se ajusta a esse número de calendários.</span><span class="sxs-lookup"><span data-stu-id="16b1c-113">When this function returns, contains the minimum **RECT** structure that fits this number of calendars.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b1c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16b1c-114">Return value</span></span>

<span data-ttu-id="16b1c-115">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="16b1c-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b1c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16b1c-116">Requirements</span></span>



| <span data-ttu-id="16b1c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b1c-117">Requirement</span></span> | <span data-ttu-id="16b1c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="16b1c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16b1c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16b1c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16b1c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16b1c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16b1c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16b1c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16b1c-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16b1c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16b1c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16b1c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="16b1c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="16b1c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

