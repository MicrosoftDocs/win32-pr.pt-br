---
description: Enumerações de áudio de núcleo
ms.assetid: 7d25be71-ffbe-4e8c-9a45-cdeb35d10292
title: Enumerações de áudio de núcleo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c786e1e18f25374a942a4140b67f0992ca7281
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457174"
---
# <a name="core-audio-enumerations"></a><span data-ttu-id="32cdc-103">Enumerações de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="32cdc-103">Core Audio Enumerations</span></span>

<span data-ttu-id="32cdc-104">Esta seção descreve as enumerações usadas pelas principais APIs de áudio no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="32cdc-104">This section describes the enumerations that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="32cdc-105">Enumeração</span><span class="sxs-lookup"><span data-stu-id="32cdc-105">Enumeration</span></span>                                                                   | <span data-ttu-id="32cdc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="32cdc-106">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32cdc-107">**\_AUDCLNT \_ BUFFERFLAGS**</span><span class="sxs-lookup"><span data-stu-id="32cdc-107">**\_AUDCLNT\_BUFFERFLAGS**</span></span>](/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags)                        | <span data-ttu-id="32cdc-108">Sinalizadores de status para um buffer de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="32cdc-108">Status flags for an audio endpoint buffer.</span></span>                                                         |
| [<span data-ttu-id="32cdc-109">**AUDCLNT \_ ShareMode**</span><span class="sxs-lookup"><span data-stu-id="32cdc-109">**AUDCLNT\_SHAREMODE**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audclnt_sharemode)                               | <span data-ttu-id="32cdc-110">O modo de compartilhamento para um fluxo.</span><span class="sxs-lookup"><span data-stu-id="32cdc-110">The sharing mode for a stream.</span></span>                                                                     |
| [<span data-ttu-id="32cdc-111">**AUDCLNT \_ streamoptions**</span><span class="sxs-lookup"><span data-stu-id="32cdc-111">**AUDCLNT\_STREAMOPTIONS**</span></span>](/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions)                       | <span data-ttu-id="32cdc-112">Define os valores que descrevem as características de um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="32cdc-112">Defines values that describe the characteristics of an audio stream.</span></span>                               |
| [<span data-ttu-id="32cdc-113">**\_categoria de fluxo de áudio \_**</span><span class="sxs-lookup"><span data-stu-id="32cdc-113">**AUDIO\_STREAM\_CATEGORY**</span></span>](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)                      | <span data-ttu-id="32cdc-114">Especifica a categoria de um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="32cdc-114">Specifies the category of an audio stream.</span></span>                                                         |
| [<span data-ttu-id="32cdc-115">**AudioSessionState**</span><span class="sxs-lookup"><span data-stu-id="32cdc-115">**AudioSessionState**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audiosessionstate)                                | <span data-ttu-id="32cdc-116">O estado de uma sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="32cdc-116">The state of an audio session.</span></span>                                                                     |
| [<span data-ttu-id="32cdc-117">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="32cdc-117">**ConnectorType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-connectortype)                                        | <span data-ttu-id="32cdc-118">O tipo de conector em uma topologia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32cdc-118">The type of connector in a device topology.</span></span>                                                        |
| [<span data-ttu-id="32cdc-119">**Flow**</span><span class="sxs-lookup"><span data-stu-id="32cdc-119">**DataFlow**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-dataflow)                                                  | <span data-ttu-id="32cdc-120">A direção do fluxo de dados de um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="32cdc-120">The data-flow direction of an audio stream.</span></span>                                                        |
| [<span data-ttu-id="32cdc-121">**EDataFlow**</span><span class="sxs-lookup"><span data-stu-id="32cdc-121">**EDataFlow**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)                                                | <span data-ttu-id="32cdc-122">A direção na qual os dados de áudio fluem entre um dispositivo de ponto de extremidade de áudio e um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="32cdc-122">The direction in which audio data flows between an audio endpoint device and a client application.</span></span> |
| [<span data-ttu-id="32cdc-123">**EndpointFormFactor**</span><span class="sxs-lookup"><span data-stu-id="32cdc-123">**EndpointFormFactor**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)                              | <span data-ttu-id="32cdc-124">Os atributos físicos gerais de um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="32cdc-124">The general physical attributes of an audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="32cdc-125">**ERole**</span><span class="sxs-lookup"><span data-stu-id="32cdc-125">**ERole**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)                                                        | <span data-ttu-id="32cdc-126">A função do sistema de um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="32cdc-126">The system role of an audio endpoint device.</span></span>                                                       |
| [<span data-ttu-id="32cdc-127">**\_ConnectionType do coletor KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="32cdc-127">**KSJACK\_SINK\_CONNECTIONTYPE**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-ksjack_sink_connectiontype)<br/> | <span data-ttu-id="32cdc-128">O tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="32cdc-128">The type of connection.</span></span><br/>                                                                 |
| [<span data-ttu-id="32cdc-129">**Parte**</span><span class="sxs-lookup"><span data-stu-id="32cdc-129">**PartType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-parttype)                                                  | <span data-ttu-id="32cdc-130">O tipo de parte de uma parte (conector ou subunidade) em uma topologia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32cdc-130">The part type of a part (connector or subunit) in a device topology.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="32cdc-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32cdc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32cdc-132">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="32cdc-132">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




