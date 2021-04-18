---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de compromisso.
ms.assetid: d7e2130b-722b-46ef-9114-17db9c95d017
title: Propriedades do compromisso (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Appointment
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 542029f9eb698c8093c43cbb8ee309b3d1f9da6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796098"
---
# <a name="appointment-properties"></a><span data-ttu-id="cf8e7-103">Propriedades do compromisso</span><span class="sxs-lookup"><span data-stu-id="cf8e7-103">Appointment Properties</span></span>

<span data-ttu-id="cf8e7-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de compromisso.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-104">Windows Portable Devices supports the following appointment properties.</span></span>



| <span data-ttu-id="cf8e7-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cf8e7-105">Property</span></span>                                   | <span data-ttu-id="cf8e7-106">VarType</span><span class="sxs-lookup"><span data-stu-id="cf8e7-106">VarType</span></span>        | <span data-ttu-id="cf8e7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf8e7-107">Description</span></span>                                                                          |
|--------------------------------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8e7-108">**\_ \_ participantes aceitos do compromisso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-108">**WPD\_APPOINTMENT\_ACCEPTED\_ATTENDEES**</span></span>  | <span data-ttu-id="cf8e7-109">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="cf8e7-110">Lista delimitada por ponto e vírgula de participantes que aceitaram o compromisso.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-110">Semicolon-delimited list of attendees who have accepted the appointment.</span></span>             |
| <span data-ttu-id="cf8e7-111">**\_ \_ participantes recusados do compromisso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-111">**WPD\_APPOINTMENT\_DECLINED\_ATTENDEES**</span></span>  | <span data-ttu-id="cf8e7-112">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-112">**VT\_LPWSTR**</span></span> | <span data-ttu-id="cf8e7-113">Lista delimitada por ponto e vírgula de participantes que recusaram o compromisso.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-113">Semicolon-delimited list of attendees who have declined the appointment.</span></span>             |
| <span data-ttu-id="cf8e7-114">**\_local do compromisso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-114">**WPD\_APPOINTMENT\_LOCATION**</span></span>             | <span data-ttu-id="cf8e7-115">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="cf8e7-115">VT\_LPWSTR</span></span>     | <span data-ttu-id="cf8e7-116">Um local amigável para leitores do compromisso, por exemplo, "prédio 5, sala 7".</span><span class="sxs-lookup"><span data-stu-id="cf8e7-116">A reader-friendly location of the appointment, for example, "Building 5, Room 7".</span></span>    |
| <span data-ttu-id="cf8e7-117">**\_ \_ participantes opcionais de compromisso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-117">**WPD\_APPOINTMENT\_OPTIONAL\_ATTENDEES**</span></span>  | <span data-ttu-id="cf8e7-118">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="cf8e7-119">Lista delimitada por ponto e vírgula de participantes opcionais para o compromisso.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-119">Semicolon-delimited list of optional attendees for the appointment.</span></span>                  |
| <span data-ttu-id="cf8e7-120">**\_ \_ participantes necessários para o compromisso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-120">**WPD\_APPOINTMENT\_REQUIRED\_ATTENDEES**</span></span>  | <span data-ttu-id="cf8e7-121">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-121">**VT\_LPWSTR**</span></span> | <span data-ttu-id="cf8e7-122">Lista delimitada por ponto-e-vírgula dos participantes necessários para o compromisso.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-122">Semicolon-delimited list of required attendees for the appointment.</span></span>                  |
| <span data-ttu-id="cf8e7-123">**\_recursos de compromisso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-123">**WPD\_APPOINTMENT\_RESOURCES**</span></span>            | <span data-ttu-id="cf8e7-124">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-124">**VT\_LPWSTR**</span></span> | <span data-ttu-id="cf8e7-125">Lista delimitada por ponto e vírgula dos recursos necessários para o compromisso.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-125">Semicolon-delimited list of resources required for the appointment.</span></span>                  |
| <span data-ttu-id="cf8e7-126">**\_ \_ participantes provisórios do compromisso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-126">**WPD\_APPOINTMENT\_TENTATIVE\_ATTENDEES**</span></span> | <span data-ttu-id="cf8e7-127">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-127">**VT\_LPWSTR**</span></span> | <span data-ttu-id="cf8e7-128">Lista delimitada por ponto e vírgula de participantes que aceitou provisoriamente o compromisso.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-128">Semicolon-delimited list of attendees who have tentatively accepted the appointment.</span></span> |
| <span data-ttu-id="cf8e7-129">**\_tipo de compromisso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-129">**WPD\_APPOINTMENT\_TYPE**</span></span>                 | <span data-ttu-id="cf8e7-130">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-130">**VT\_LPWSTR**</span></span> | <span data-ttu-id="cf8e7-131">O tipo de compromisso, por exemplo, "pessoal", "negócios" e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-131">The type of appointment, for example,"Personal", "Business", and so on.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="cf8e7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf8e7-132">Requirements</span></span>



| <span data-ttu-id="cf8e7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf8e7-133">Requirement</span></span> | <span data-ttu-id="cf8e7-134">Valor</span><span class="sxs-lookup"><span data-stu-id="cf8e7-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8e7-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf8e7-135">Header</span></span><br/> | <dl> <span data-ttu-id="cf8e7-136"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf8e7-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8e7-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf8e7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8e7-138">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-138">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




