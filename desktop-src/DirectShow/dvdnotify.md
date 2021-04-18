---
description: O evento DVDNotify notifica um aplicativo sobre vários eventos de DVD e instruções de disco diferentes.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782198"
---
# <a name="dvdnotify"></a><span data-ttu-id="6364c-103">DVDNotify</span><span class="sxs-lookup"><span data-stu-id="6364c-103">DVDNotify</span></span>

> [!Note]  
> <span data-ttu-id="6364c-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6364c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6364c-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6364c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6364c-106">O `DVDNotify` evento notifica um aplicativo sobre vários eventos de DVD e instruções de disco diferentes.</span><span class="sxs-lookup"><span data-stu-id="6364c-106">The `DVDNotify` event notifies an application of many different DVD events and disc instructions.</span></span>

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a><span data-ttu-id="6364c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6364c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6364c-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span><span class="sxs-lookup"><span data-stu-id="6364c-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span></span>
</dt> <dd>

<span data-ttu-id="6364c-109">Especifica o código de notificação de evento de DVD.</span><span class="sxs-lookup"><span data-stu-id="6364c-109">Specifies the DVD event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6364c-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span><span class="sxs-lookup"><span data-stu-id="6364c-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span></span>
</dt> <dd>

<span data-ttu-id="6364c-111">Pode conter informações adicionais relacionadas ao evento.</span><span class="sxs-lookup"><span data-stu-id="6364c-111">Can contain additional information related to the event.</span></span>

</dd> <dt>

<span data-ttu-id="6364c-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span><span class="sxs-lookup"><span data-stu-id="6364c-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span></span>
</dt> <dd>

<span data-ttu-id="6364c-113">Pode conter informações adicionais relacionadas ao evento.</span><span class="sxs-lookup"><span data-stu-id="6364c-113">Can contain additional information related to the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6364c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6364c-114">Remarks</span></span>

<span data-ttu-id="6364c-115">Os [códigos de notificação de eventos de DVD](dvd-notification-codes.md) fornecem uma explicação completa de todos os códigos de notificação de eventos de DVD e seus parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6364c-115">[DVD Event Notification Codes](dvd-notification-codes.md) gives a full explanation of all DVD event notification codes and their parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6364c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6364c-116">Requirements</span></span>



| <span data-ttu-id="6364c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6364c-117">Requirement</span></span> | <span data-ttu-id="6364c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6364c-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6364c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6364c-119">Header</span></span><br/> | <dl> <span data-ttu-id="6364c-120"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="6364c-120"><dt>Segment.h</dt></span></span> </dl> |



 

 




