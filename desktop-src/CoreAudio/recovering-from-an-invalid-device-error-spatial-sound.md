---
description: Recuperando de um erro de Invalid-Device (som espacial)
title: Recuperando de um erro de Invalid-Device (som espacial)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089508"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a><span data-ttu-id="f41fa-103">Recuperando de um erro de Invalid-Device (som espacial)</span><span class="sxs-lookup"><span data-stu-id="f41fa-103">Recovering from an Invalid-Device Error (Spatial Sound)</span></span>

<span data-ttu-id="f41fa-104">Muitos dos métodos da API de áudio espacial da Microsoft, como [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)e [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), retornam códigos de erro se o dispositivo de ponto de extremidade de áudio que o aplicativo cliente está usando se tornar inválido ou se o formato de renderização de áudio espacial for alterado no ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="f41fa-104">Many of the methods of the Microsoft Spatial Audio API, such as [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream), and [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), return error codes if the audio endpoint device that the client application is using becomes invalid or the spatial audio rendering format is changed on the endpoint.</span></span> <span data-ttu-id="f41fa-105">Esses códigos de erro indicam que o dispositivo de ponto de extremidade foi desconectado ou que o hardware de áudio ou os recursos de hardware associados foram reconfigurados, desabilitados, removidos, o modo de áudio espacial foi alterado ou tornou-se indisponível para uso.</span><span class="sxs-lookup"><span data-stu-id="f41fa-105">These error codes indicates that the endpoint device has been unplugged, or that the audio hardware or associated hardware resources have been reconfigured, disabled, removed, spatial audio mode is changed or otherwise made unavailable for use.</span></span> <span data-ttu-id="f41fa-106">Frequentemente, o aplicativo pode se recuperar desse erro.</span><span class="sxs-lookup"><span data-stu-id="f41fa-106">Frequently, the application can recover from this error.</span></span>

<span data-ttu-id="f41fa-107">Os códigos de erro que indicam um erro de dispositivo inválido incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f41fa-107">Error codes that indicate an invalid-device error include the following:</span></span>

- <span data-ttu-id="f41fa-108">SPTLAUDCLNT_E_DESTROYED</span><span class="sxs-lookup"><span data-stu-id="f41fa-108">SPTLAUDCLNT_E_DESTROYED</span></span>
- <span data-ttu-id="f41fa-109">AUDCLNT_E_DEVICE_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="f41fa-109">AUDCLNT_E_DEVICE_INVALIDATED</span></span>
- <span data-ttu-id="f41fa-110">AUDCLNT_E_RESOURCES_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="f41fa-110">AUDCLNT_E_RESOURCES_INVALIDATED</span></span>
- <span data-ttu-id="f41fa-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span><span class="sxs-lookup"><span data-stu-id="f41fa-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span></span>
- <span data-ttu-id="f41fa-112">SPTLAUDCLNT_E_INTERNAL</span><span class="sxs-lookup"><span data-stu-id="f41fa-112">SPTLAUDCLNT_E_INTERNAL</span></span>

## <a name="strategies-for-handling-invalid-device-errors"></a><span data-ttu-id="f41fa-113">Estratégias para lidar com erros de dispositivo inválido</span><span class="sxs-lookup"><span data-stu-id="f41fa-113">Strategies for handling invalid-device errors</span></span>

<span data-ttu-id="f41fa-114">A estratégia recomendada para a recuperação de um erro de dispositivo inválido depende se o aplicativo seleciona automaticamente um dispositivo específico com base em requisitos internos ou permite que o usuário selecione explicitamente um dispositivo de uma lista de dispositivos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f41fa-114">The recommended strategy for recovering from an invalid-device error depends on whether the application automatically selects a specific device based on internal requirements or it allows the user to explicitly select a device from a list of available devices.</span></span> 

### <a name="default-audio-device"></a><span data-ttu-id="f41fa-115">Dispositivo de áudio padrão</span><span class="sxs-lookup"><span data-stu-id="f41fa-115">Default audio device</span></span>

<span data-ttu-id="f41fa-116">Se o aplicativo selecionar automaticamente o dispositivo padrão, use as etapas a seguir para recuperar.</span><span class="sxs-lookup"><span data-stu-id="f41fa-116">If the application automatically selects the default device, use the following steps to recover.</span></span>

1. <span data-ttu-id="f41fa-117">Libere a interface [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) e [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) e quaisquer outras interfaces de áudio espaciais usadas para renderização.</span><span class="sxs-lookup"><span data-stu-id="f41fa-117">Release the [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) and [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interface and any other spatial audio interfaces that are used for rendering.</span></span> 
1. <span data-ttu-id="f41fa-118">Chame [IMMDeviceEnumerator:: GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter o dispositivo de áudio padrão atual.</span><span class="sxs-lookup"><span data-stu-id="f41fa-118">Call [IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the current default audio device.</span></span>
1. <span data-ttu-id="f41fa-119">Tentativa de ativar **ISpatialAudioClient** no dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="f41fa-119">Attempt to activate **ISpatialAudioClient** on the audio device.</span></span>
1. <span data-ttu-id="f41fa-120">Ative o **ISpatialAudioObjectRenderStream**.</span><span class="sxs-lookup"><span data-stu-id="f41fa-120">Activate **ISpatialAudioObjectRenderStream**.</span></span> 

### <a name="specifically-selected-audio-device"></a><span data-ttu-id="f41fa-121">Dispositivo de áudio especificamente selecionado</span><span class="sxs-lookup"><span data-stu-id="f41fa-121">Specifically selected audio device</span></span>

<span data-ttu-id="f41fa-122">Se o aplicativo selecionar um dispositivo de áudio específico, use as etapas a seguir para recuperar.</span><span class="sxs-lookup"><span data-stu-id="f41fa-122">If the application selects a specific audio device, use the following steps to recover.</span></span>

1. <span data-ttu-id="f41fa-123">Libere a interface ISpatialAudioObjectRenderStream e quaisquer outras interfaces de áudio espaciais usadas para renderização, mas não libere **ISpatialAudioClient**.</span><span class="sxs-lookup"><span data-stu-id="f41fa-123">Release the ISpatialAudioObjectRenderStream interface and any other spatial audio interfaces that are used for rendering, but don't release **ISpatialAudioClient**.</span></span>
1. <span data-ttu-id="f41fa-124">Use a instância **ISpatialAudioClient** atual para ativar o **ISpatialAudioObjectRenderStream**.</span><span class="sxs-lookup"><span data-stu-id="f41fa-124">Use the current **ISpatialAudioClient** instance to activate **ISpatialAudioObjectRenderStream**.</span></span>

<span data-ttu-id="f41fa-125">Observe que, para ambas as estratégias listadas acima, as mesmas etapas podem ser aplicadas a aplicativos que usam as interfaces [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) ou [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) .</span><span class="sxs-lookup"><span data-stu-id="f41fa-125">Note that for both strategies listed above, the same steps can be applied to applications that use the [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) or [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) interfaces.</span></span> <span data-ttu-id="f41fa-126">Basta substituir **ISpatialAudioObjectRenderStream** nas etapas acima pelas interfaces Metadata ou HRTF.</span><span class="sxs-lookup"><span data-stu-id="f41fa-126">Simply replace **ISpatialAudioObjectRenderStream** in the above steps with the metadata or Hrtf interfaces.</span></span>


## <a name="related-topics"></a><span data-ttu-id="f41fa-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f41fa-127">Related topics</span></span>

<dl> <span data-ttu-id="f41fa-128"><dt>
[Recuperando de um erro](recovering-from-an-invalid-device-error.md) 
 de Invalid-Device [Gerenciamento de fluxo](stream-management.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="f41fa-128"><dt>
[Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md)
[Stream Management](stream-management.md)
</dt> </span></span></dl>

 

 



