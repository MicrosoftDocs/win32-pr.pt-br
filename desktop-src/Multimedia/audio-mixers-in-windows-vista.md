---
title: Mixers de áudio no Windows Vista
description: Mixers de áudio no Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- áudio multimídia, mixers de áudio do Windows Vista
- áudio, mixers de áudio do Windows Vista
- mixers de áudio, Windows Vista
- mixers, Windows Vista
- Mixers de áudio do Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104558762"
---
# <a name="audio-mixers-in-windows-vista"></a><span data-ttu-id="16c96-108">Mixers de áudio no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16c96-108">Audio Mixers in Windows Vista</span></span>

<span data-ttu-id="16c96-109">A partir do Windows Vista, alguns controles de mixer são implementados em software em vez de hardware.</span><span class="sxs-lookup"><span data-stu-id="16c96-109">Starting in Windows Vista, some mixer controls are implemented in software rather than hardware.</span></span> <span data-ttu-id="16c96-110">Por exemplo, os controles de volume são implementados usando a API de sessão de áudio do Windows (WASAPI).</span><span class="sxs-lookup"><span data-stu-id="16c96-110">For example, the volume controls are implemented using the Windows audio session API (WASAPI).</span></span> <span data-ttu-id="16c96-111">Esses controles não afetam diretamente as configurações de hardware.</span><span class="sxs-lookup"><span data-stu-id="16c96-111">These controls do not directly affect hardware settings.</span></span> <span data-ttu-id="16c96-112">Além disso, eles são associados a uma sessão de áudio específica do processo, portanto, as alterações afetam o aplicativo de chamada, mas não afetam outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="16c96-112">In addition, they are associated with a process-specific audio session, so changes affect the calling application but do not affect other applications.</span></span>

<span data-ttu-id="16c96-113">Cada dispositivo de ponto de extremidade de áudio tem um layout de mixer padrão, implementado no software.</span><span class="sxs-lookup"><span data-stu-id="16c96-113">Each audio endpoint device has a standard mixer layout, implemented in software.</span></span>

-   <span data-ttu-id="16c96-114">Cada ponto de extremidade de renderização de áudio contém uma linha de destino que contém o seguinte:</span><span class="sxs-lookup"><span data-stu-id="16c96-114">Each audio rendering endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="16c96-115">Controle de volume</span><span class="sxs-lookup"><span data-stu-id="16c96-115">Volume control</span></span>
    -   <span data-ttu-id="16c96-116">Controle sem áudio</span><span class="sxs-lookup"><span data-stu-id="16c96-116">Mute control</span></span>
    -   <span data-ttu-id="16c96-117">Linha de origem: onda-saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="16c96-117">Source line: Waveform-audio output.</span></span>
    -   <span data-ttu-id="16c96-118">Linha de origem: CD de áudio.</span><span class="sxs-lookup"><span data-stu-id="16c96-118">Source line: Audio CD.</span></span>
-   <span data-ttu-id="16c96-119">Cada ponto de extremidade de captura de áudio contém uma linha de destino que contém o seguinte:</span><span class="sxs-lookup"><span data-stu-id="16c96-119">Each audio capture endpoint contains one destination line that contains the following:</span></span>
    -   <span data-ttu-id="16c96-120">Controle de volume</span><span class="sxs-lookup"><span data-stu-id="16c96-120">Volume control</span></span>
    -   <span data-ttu-id="16c96-121">Controle sem áudio</span><span class="sxs-lookup"><span data-stu-id="16c96-121">Mute control</span></span>
    -   <span data-ttu-id="16c96-122">Linha de origem: formato de onda-entrada de áudio.</span><span class="sxs-lookup"><span data-stu-id="16c96-122">Source line: Waveform-audio input.</span></span> <span data-ttu-id="16c96-123">O tipo de componente depende do dispositivo de entrada, por exemplo, um microfone.</span><span class="sxs-lookup"><span data-stu-id="16c96-123">The component type depends on the input device— for example, a microphone.</span></span>

<span data-ttu-id="16c96-124">Cada linha de origem contém um controle de volume e um controle sem áudio.</span><span class="sxs-lookup"><span data-stu-id="16c96-124">Each source line contains a volume control and a mute control.</span></span> <span data-ttu-id="16c96-125">O diagrama a seguir mostra os componentes de pontos de extremidade de renderização e captura de pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="16c96-125">The following diagram shows the components of render endpoints and capture endpoints.</span></span>

![layouts de mixer padrão](images/mixer1.gif)

<span data-ttu-id="16c96-127">Todos os controles de um ponto de extremidade manipulam o mesmo controle de software subjacente.</span><span class="sxs-lookup"><span data-stu-id="16c96-127">All of the controls for an endpoint manipulate the same underlying software control.</span></span> <span data-ttu-id="16c96-128">Portanto, se você alterar as configurações em um controle, receberá uma notificação de alteração de controle nos outros controles.</span><span class="sxs-lookup"><span data-stu-id="16c96-128">Therefore, if you change the settings on one control, you will receive a control change notification on the other controls.</span></span> <span data-ttu-id="16c96-129">(Consulte [**\_ mudança de \_ controle \_ de MIXM mm**](mm-mixm-control-change.md).)</span><span class="sxs-lookup"><span data-stu-id="16c96-129">(See [**MM\_MIXM\_CONTROL\_CHANGE**](mm-mixm-control-change.md).)</span></span>

<span data-ttu-id="16c96-130">Esse layout padrão é fornecido para compatibilidade com os aplicativos existentes que usam as funções do mixer de áudio.</span><span class="sxs-lookup"><span data-stu-id="16c96-130">This standard layout is provided for compatibility with existing applications that use the audio mixer functions.</span></span> <span data-ttu-id="16c96-131">Os novos aplicativos devem evitar o uso dessas funções.</span><span class="sxs-lookup"><span data-stu-id="16c96-131">New applications should avoid using these functions.</span></span>

 

 




