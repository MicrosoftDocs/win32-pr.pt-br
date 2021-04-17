---
description: Sinaliza que o número de ângulos disponíveis foi alterado ou que o número de ângulo atual foi alterado.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789900"
---
# <a name="ec_dvd_angle_change"></a><span data-ttu-id="42a7e-103">\_alteração de \_ ângulo do DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="42a7e-103">EC\_DVD\_ANGLE\_CHANGE</span></span>

<span data-ttu-id="42a7e-104">Sinaliza que o número de ângulos disponíveis foi alterado ou que o número de ângulo atual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="42a7e-104">Signals that either the number of available angles changed or that the current angle number changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="42a7e-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42a7e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a7e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="42a7e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="42a7e-107">Valor **DWORD** que indica o número de ângulos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="42a7e-107">**DWORD** value indicating the number of available angles.</span></span> <span data-ttu-id="42a7e-108">Quando o número de ângulos disponíveis é 1, o vídeo atual não é multiângulo.</span><span class="sxs-lookup"><span data-stu-id="42a7e-108">When the number of available angles is 1, the current video is not multiangle.</span></span>

</dd> <dt>

<span data-ttu-id="42a7e-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="42a7e-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="42a7e-110">Valor **DWORD** que indica o número do ângulo atual.</span><span class="sxs-lookup"><span data-stu-id="42a7e-110">**DWORD** value indicating the current angle number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42a7e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="42a7e-111">Remarks</span></span>

<span data-ttu-id="42a7e-112">Os números de ângulo variam de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="42a7e-112">Angle numbers range from 1 to 9.</span></span>

<span data-ttu-id="42a7e-113">O número do ângulo atual pode ser alterado automaticamente com um comando de navegação criado no disco, bem como por meio do controle de aplicativo usando a interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="42a7e-113">The current angle number can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="42a7e-114">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="42a7e-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a7e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a7e-115">Requirements</span></span>



| <span data-ttu-id="42a7e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a7e-116">Requirement</span></span> | <span data-ttu-id="42a7e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="42a7e-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a7e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42a7e-118">Header</span></span><br/> | <dl> <span data-ttu-id="42a7e-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42a7e-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a7e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="42a7e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a7e-121">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="42a7e-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="42a7e-122">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="42a7e-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="42a7e-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="42a7e-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




