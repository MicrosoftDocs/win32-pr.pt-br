---
description: A interface ITTime é uma interface específica de provedor para um objeto de blob de conferência SDP (Session Descriptor Protocol).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Interface ITTime (Sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758407"
---
# <a name="ittime-interface"></a><span data-ttu-id="3c3b0-103">Interface ITTime</span><span class="sxs-lookup"><span data-stu-id="3c3b0-103">ITTime interface</span></span>

<span data-ttu-id="3c3b0-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3c3b0-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3c3b0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3c3b0-106">A interface **ITTime** é uma interface específica de provedor para um objeto de blob de conferência SDP (Session Descriptor Protocol).</span><span class="sxs-lookup"><span data-stu-id="3c3b0-106">The **ITTime** interface is a provider-specific interface for a Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="3c3b0-107">Ele fornece acesso a um conjunto de tempos de ativação para a sessão.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-107">It provides access to a set of activation times for the session.</span></span> <span data-ttu-id="3c3b0-108">Os métodos [**IEnumTime:: Next**](ienumtime-next.md) e [**ITTimeCollection:: Create**](ittimecollection-create.md) criam a interface **ITTime** .</span><span class="sxs-lookup"><span data-stu-id="3c3b0-108">The [**IEnumTime::Next**](ienumtime-next.md) and [**ITTimeCollection::Create**](ittimecollection-create.md) methods create the **ITTime** interface.</span></span>

## <a name="members"></a><span data-ttu-id="3c3b0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="3c3b0-109">Members</span></span>

<span data-ttu-id="3c3b0-110">A interface **ITTime** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3c3b0-110">The **ITTime** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3c3b0-111">**ITTime** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3c3b0-111">**ITTime** also has these types of members:</span></span>

-   [<span data-ttu-id="3c3b0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c3b0-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3c3b0-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3c3b0-113">Methods</span></span>

<span data-ttu-id="3c3b0-114">A interface **ITTime** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-114">The **ITTime** interface has these methods.</span></span>



| <span data-ttu-id="3c3b0-115">Método</span><span class="sxs-lookup"><span data-stu-id="3c3b0-115">Method</span></span>                                         | <span data-ttu-id="3c3b0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c3b0-116">Description</span></span>                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="3c3b0-117">**obter \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="3c3b0-117">**get\_StartTime**</span></span>](ittime-get-starttime.md) | <span data-ttu-id="3c3b0-118">Obtém o valor de hora de início do NTP de 32 bits (protocolo NTP).</span><span class="sxs-lookup"><span data-stu-id="3c3b0-118">Gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span><br/> |
| [<span data-ttu-id="3c3b0-119">**obter \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="3c3b0-119">**get\_StopTime**</span></span>](ittime-get-stoptime.md)   | <span data-ttu-id="3c3b0-120">Obtém o valor de hora de término do NTP.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-120">Gets the NTP ending time value.</span></span><br/>                                  |
| [<span data-ttu-id="3c3b0-121">**colocar \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="3c3b0-121">**put\_StartTime**</span></span>](ittime-put-starttime.md) | <span data-ttu-id="3c3b0-122">Define o valor de hora de início de NTP de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-122">Sets the 32-bit NTP starting time value.</span></span><br/>                         |
| [<span data-ttu-id="3c3b0-123">**colocar \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="3c3b0-123">**put\_StopTime**</span></span>](ittime-put-stoptime.md)   | <span data-ttu-id="3c3b0-124">Define o valor de hora de término do NTP.</span><span class="sxs-lookup"><span data-stu-id="3c3b0-124">Sets the NTP ending time value.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="3c3b0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c3b0-125">Requirements</span></span>



| <span data-ttu-id="3c3b0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c3b0-126">Requirement</span></span> | <span data-ttu-id="3c3b0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3c3b0-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c3b0-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3c3b0-128">TAPI version</span></span><br/> | <span data-ttu-id="3c3b0-129">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3c3b0-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3c3b0-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c3b0-130">Header</span></span><br/>       | <dl> <span data-ttu-id="3c3b0-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c3b0-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c3b0-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c3b0-132">Library</span></span><br/>      | <dl> <span data-ttu-id="3c3b0-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c3b0-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3c3b0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3c3b0-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="3c3b0-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c3b0-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

