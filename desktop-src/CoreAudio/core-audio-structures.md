---
description: Estruturas de áudio de núcleo
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Estruturas de áudio de núcleo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753560"
---
# <a name="core-audio-structures"></a><span data-ttu-id="d0a11-103">Estruturas de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="d0a11-103">Core Audio Structures</span></span>

<span data-ttu-id="d0a11-104">Esta seção descreve as estruturas usadas pelas principais APIs de áudio no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d0a11-104">This section describes the structures that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="d0a11-105">Estrutura</span><span class="sxs-lookup"><span data-stu-id="d0a11-105">Structure</span></span>                                                                     | <span data-ttu-id="d0a11-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0a11-106">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0a11-107">**\_dados de \_ notificação por volume de áudio \_**</span><span class="sxs-lookup"><span data-stu-id="d0a11-107">**AUDIO\_VOLUME\_NOTIFICATION\_DATA**</span></span>](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | <span data-ttu-id="d0a11-108">Descreve uma alteração no nível do volume ou estado de mudo de um dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="d0a11-108">Describes a change in the volume level or muting state of an audio endpoint device.</span></span>                                                                                 |
| [<span data-ttu-id="d0a11-109">**\_ \_ params de ativação de áudio DirectX \_**</span><span class="sxs-lookup"><span data-stu-id="d0a11-109">**DIRECTX\_AUDIO\_ACTIVATION\_PARAMS**</span></span>](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | <span data-ttu-id="d0a11-110">Especifica os parâmetros de inicialização para um fluxo do DirectSound.</span><span class="sxs-lookup"><span data-stu-id="d0a11-110">Specifies the initialization parameters for a DirectSound stream.</span></span>                                                                                                   |
| [<span data-ttu-id="d0a11-111">**Descrição de KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="d0a11-111">**KSJACK\_DESCRIPTION**</span></span>](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | <span data-ttu-id="d0a11-112">Recuperado por meio de [**IKsJackDescription:: GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); descreve uma tomada de áudio.</span><span class="sxs-lookup"><span data-stu-id="d0a11-112">Retrieved through [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describes an audio jack.</span></span>                                 |
| [<span data-ttu-id="d0a11-113">**KSJACK \_ DESCRIPTION2**</span><span class="sxs-lookup"><span data-stu-id="d0a11-113">**KSJACK\_DESCRIPTION2**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | <span data-ttu-id="d0a11-114">Recuperado por meio de [**IKsJackDescription2:: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); descreve uma tomada de áudio.</span><span class="sxs-lookup"><span data-stu-id="d0a11-114">Retrieved through [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describes an audio jack.</span></span> <br/>                 |
| [<span data-ttu-id="d0a11-115">**\_informações do coletor KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="d0a11-115">**KSJACK\_SINK\_INFORMATION**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | <span data-ttu-id="d0a11-116">Recuperado por meio de [**IKsJackSinkInformation:: GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); Descreve um coletor de tomada de áudio.</span><span class="sxs-lookup"><span data-stu-id="d0a11-116">Retrieved through [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describes an audio jack sink.</span></span><br/> |
| [<span data-ttu-id="d0a11-117">**LUID**</span><span class="sxs-lookup"><span data-stu-id="d0a11-117">**LUID**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | <span data-ttu-id="d0a11-118">Armazena o identificador da porta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0a11-118">Stores the video port identifier.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="d0a11-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0a11-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0a11-120">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="d0a11-120">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




