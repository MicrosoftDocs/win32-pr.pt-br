---
title: Enumeração de TransportState
description: Define os Estados de transporte disponíveis, conforme definido pelas diretrizes de UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API de streaming de mídia de enumeração de transportestate
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771460"
---
# <a name="transportstate-enumeration"></a><span data-ttu-id="ad776-104">Enumeração de TransportState</span><span class="sxs-lookup"><span data-stu-id="ad776-104">TransportState enumeration</span></span>

<span data-ttu-id="ad776-105">Define os Estados de transporte disponíveis, conforme definido pelas diretrizes de UPnP.</span><span class="sxs-lookup"><span data-stu-id="ad776-105">Defines the available transport states as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad776-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad776-106">Syntax</span></span>


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a><span data-ttu-id="ad776-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="ad776-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ad776-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Conhecidos**</span><span class="sxs-lookup"><span data-stu-id="ad776-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="ad776-109">Estado do dispositivo errado.</span><span class="sxs-lookup"><span data-stu-id="ad776-109">Erroneous device state.</span></span>

</dd> <dt>

<span data-ttu-id="ad776-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Interrompido**</span><span class="sxs-lookup"><span data-stu-id="ad776-110"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped**</span></span>
</dt> <dd>

<span data-ttu-id="ad776-111">O transporte do dispositivo s está em um estado parado.</span><span class="sxs-lookup"><span data-stu-id="ad776-111">The device s transport is in a stopped state.</span></span>

</dd> <dt>

<span data-ttu-id="ad776-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Jogando**</span><span class="sxs-lookup"><span data-stu-id="ad776-112"><span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Playing**</span></span>
</dt> <dd>

<span data-ttu-id="ad776-113">O transporte do dispositivo está em estado de execução.</span><span class="sxs-lookup"><span data-stu-id="ad776-113">The device s transport is in a playing state.</span></span>

</dd> <dt>

<span data-ttu-id="ad776-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição**</span><span class="sxs-lookup"><span data-stu-id="ad776-114"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning**</span></span>
</dt> <dd>

<span data-ttu-id="ad776-115">O transporte do dispositivo s está em um estado de transição, o que resultará em outro valor de estado.</span><span class="sxs-lookup"><span data-stu-id="ad776-115">The device s transport is in a transitioning state which will result in another state value.</span></span>

</dd> <dt>

<span data-ttu-id="ad776-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Em pausa**</span><span class="sxs-lookup"><span data-stu-id="ad776-116"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused**</span></span>
</dt> <dd>

<span data-ttu-id="ad776-117">O transporte do dispositivo s está em um estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="ad776-117">The device s transport is in a paused state.</span></span>

</dd> <dt>

<span data-ttu-id="ad776-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Registra**</span><span class="sxs-lookup"><span data-stu-id="ad776-118"><span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Recording**</span></span>
</dt> <dd>

<span data-ttu-id="ad776-119">O transporte do dispositivo s está em um estado de gravação.</span><span class="sxs-lookup"><span data-stu-id="ad776-119">The device s transport is in a recording state.</span></span>

</dd> <dt>

<span data-ttu-id="ad776-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span><span class="sxs-lookup"><span data-stu-id="ad776-120"><span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**</span></span>
</dt> <dd>

<span data-ttu-id="ad776-121">O transporte do dispositivo s não tem um URI definido para reprodução.</span><span class="sxs-lookup"><span data-stu-id="ad776-121">The device s transport does not have an URI set for playback.</span></span>

</dd> <dt>

<span data-ttu-id="ad776-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Última**</span><span class="sxs-lookup"><span data-stu-id="ad776-122"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="ad776-123">O estado anterior do dispositivo para o estado de transporte atual.</span><span class="sxs-lookup"><span data-stu-id="ad776-123">The device s previous state to the current transport state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad776-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad776-124">Requirements</span></span>



| <span data-ttu-id="ad776-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad776-125">Requirement</span></span> | <span data-ttu-id="ad776-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ad776-126">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad776-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="ad776-127">IDL</span></span><br/> | <dl> <span data-ttu-id="ad776-128"><dt>Windows. Media. streaming. idl (referência Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="ad776-128"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





