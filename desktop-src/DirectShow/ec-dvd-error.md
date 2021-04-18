---
description: Sinaliza uma condição de erro de DVD.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 3b338889836bf78a334784ea66c0e346e9f6b672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766997"
---
# <a name="ec_dvd_error"></a><span data-ttu-id="412de-103">\_erro de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="412de-103">EC\_DVD\_ERROR</span></span>

<span data-ttu-id="412de-104">Sinaliza uma condição de erro de DVD.</span><span class="sxs-lookup"><span data-stu-id="412de-104">Signals a DVD error condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="412de-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="412de-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="412de-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="412de-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="412de-107">Valor **DWORD** que indica a condição de erro.</span><span class="sxs-lookup"><span data-stu-id="412de-107">**DWORD** value indicating the error condition.</span></span> <span data-ttu-id="412de-108">Membro do tipo de dados enumerado de [**\_ erro de DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) .</span><span class="sxs-lookup"><span data-stu-id="412de-108">Member of the [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="412de-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="412de-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="412de-110">O significado depende do valor de *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="412de-110">Meaning depends on the value of *lParam1*.</span></span> <span data-ttu-id="412de-111">Consulte [**\_ erro de DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="412de-111">See [**DVD\_ERROR**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error) for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="412de-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="412de-112">Remarks</span></span>

<span data-ttu-id="412de-113">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="412de-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="412de-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="412de-114">Requirements</span></span>



| <span data-ttu-id="412de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="412de-115">Requirement</span></span> | <span data-ttu-id="412de-116">Valor</span><span class="sxs-lookup"><span data-stu-id="412de-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="412de-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="412de-117">Header</span></span><br/> | <dl> <span data-ttu-id="412de-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="412de-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="412de-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="412de-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412de-120">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="412de-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="412de-121">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="412de-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="412de-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="412de-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




