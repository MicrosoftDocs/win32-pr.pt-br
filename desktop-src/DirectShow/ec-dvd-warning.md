---
description: Sinaliza uma condição de aviso de DVD.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789643"
---
# <a name="ec_dvd_warning"></a><span data-ttu-id="33391-103">\_aviso de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="33391-103">EC\_DVD\_WARNING</span></span>

<span data-ttu-id="33391-104">Sinaliza uma condição de aviso de DVD.</span><span class="sxs-lookup"><span data-stu-id="33391-104">Signals a DVD warning condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="33391-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33391-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33391-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="33391-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="33391-107">Valor **DWORD** que indica a condição de aviso.</span><span class="sxs-lookup"><span data-stu-id="33391-107">**DWORD** value indicating the warning condition.</span></span> <span data-ttu-id="33391-108">Membro do tipo de dados enumerado de [**\_ aviso de DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) .</span><span class="sxs-lookup"><span data-stu-id="33391-108">Member of the [**DVD\_WARNING**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="33391-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="33391-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="33391-110">Se *pParam1* for igual a \_ aviso \_ de DVD aberto, \_ a busca de aviso de DVD \_ ou o aviso de DVD será \_ \_ lido, então *lParam2* conterá o último código de erro retornado de **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="33391-110">If *pParam1* equals DVD\_WARNING\_Open, DVD\_WARNING\_Seek, or DVD\_WARNING\_Read, then *lParam2* contains the last error code returned from **GetLastError**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33391-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33391-111">Requirements</span></span>



| <span data-ttu-id="33391-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="33391-112">Requirement</span></span> | <span data-ttu-id="33391-113">Valor</span><span class="sxs-lookup"><span data-stu-id="33391-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33391-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33391-114">Header</span></span><br/> | <dl> <span data-ttu-id="33391-115"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33391-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33391-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="33391-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33391-117">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="33391-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="33391-118">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="33391-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="33391-119">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="33391-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




