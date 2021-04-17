---
title: Valores de desenho personalizados (CommCtrl. h)
description: Esta seção lista os valores usados para identificar as partes de um controle TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748099"
---
# <a name="custom-draw-values"></a><span data-ttu-id="e3e55-103">Valores de desenho personalizados</span><span class="sxs-lookup"><span data-stu-id="e3e55-103">Custom Draw Values</span></span>

<span data-ttu-id="e3e55-104">Esta seção lista os valores usados para identificar as partes de um controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e3e55-104">This section lists the values used to identify a Trackbar control's parts.</span></span>



| <span data-ttu-id="e3e55-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e3e55-105">Constant</span></span>                                                                                                                                                   | <span data-ttu-id="e3e55-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3e55-106">Description</span></span>                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="e3e55-107"><dt>**\_canal TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="e3e55-107"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="e3e55-108">Identifica o canal no qual o marcador de Thumb do controle de TrackBar desliza.</span><span class="sxs-lookup"><span data-stu-id="e3e55-108">Identifies the channel that the trackbar control's thumb marker slides along.</span></span><br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="e3e55-109"><dt>**TBCD \_ Thumb**</dt></span><span class="sxs-lookup"><span data-stu-id="e3e55-109"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="e3e55-110">Identifica o marcador de miniatura do controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e3e55-110">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="e3e55-111">Essa é a parte do controle que o usuário move.</span><span class="sxs-lookup"><span data-stu-id="e3e55-111">This is the part of the control that the user moves.</span></span><br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="e3e55-112"><dt>**TBCD \_ TICS**</dt></span><span class="sxs-lookup"><span data-stu-id="e3e55-112"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="e3e55-113">Identifica as marcas de escala que são exibidas ao longo da borda do controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e3e55-113">Identifies the tick marks that are displayed along the trackbar control's edge.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="e3e55-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3e55-114">Remarks</span></span>

<span data-ttu-id="e3e55-115">Os valores personalizados de desenho, por exemplo, são especificados no membro **dwItemSpec** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .</span><span class="sxs-lookup"><span data-stu-id="e3e55-115">Custom Draw values, for example, are specified in the **dwItemSpec** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e55-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3e55-116">Requirements</span></span>



| <span data-ttu-id="e3e55-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3e55-117">Requirement</span></span> | <span data-ttu-id="e3e55-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e3e55-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e55-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3e55-119">Header</span></span><br/> | <dl> <span data-ttu-id="e3e55-120"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3e55-120"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





