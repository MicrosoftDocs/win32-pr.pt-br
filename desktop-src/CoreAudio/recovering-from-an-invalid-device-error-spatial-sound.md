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
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>Recuperando de um erro de Invalid-Device (som espacial)

Muitos dos métodos da API de áudio espacial da Microsoft, como [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)e [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), retornam códigos de erro se o dispositivo de ponto de extremidade de áudio que o aplicativo cliente está usando se tornar inválido ou se o formato de renderização de áudio espacial for alterado no ponto de extremidade. Esses códigos de erro indicam que o dispositivo de ponto de extremidade foi desconectado ou que o hardware de áudio ou os recursos de hardware associados foram reconfigurados, desabilitados, removidos, o modo de áudio espacial foi alterado ou tornou-se indisponível para uso. Frequentemente, o aplicativo pode se recuperar desse erro.

Os códigos de erro que indicam um erro de dispositivo inválido incluem o seguinte:

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>Estratégias para lidar com erros de dispositivo inválido

A estratégia recomendada para a recuperação de um erro de dispositivo inválido depende se o aplicativo seleciona automaticamente um dispositivo específico com base em requisitos internos ou permite que o usuário selecione explicitamente um dispositivo de uma lista de dispositivos disponíveis. 

### <a name="default-audio-device"></a>Dispositivo de áudio padrão

Se o aplicativo selecionar automaticamente o dispositivo padrão, use as etapas a seguir para recuperar.

1. Libere a interface [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) e [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) e quaisquer outras interfaces de áudio espaciais usadas para renderização. 
1. Chame [IMMDeviceEnumerator:: GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter o dispositivo de áudio padrão atual.
1. Tentativa de ativar **ISpatialAudioClient** no dispositivo de áudio.
1. Ative o **ISpatialAudioObjectRenderStream**. 

### <a name="specifically-selected-audio-device"></a>Dispositivo de áudio especificamente selecionado

Se o aplicativo selecionar um dispositivo de áudio específico, use as etapas a seguir para recuperar.

1. Libere a interface ISpatialAudioObjectRenderStream e quaisquer outras interfaces de áudio espaciais usadas para renderização, mas não libere **ISpatialAudioClient**.
1. Use a instância **ISpatialAudioClient** atual para ativar o **ISpatialAudioObjectRenderStream**.

Observe que, para ambas as estratégias listadas acima, as mesmas etapas podem ser aplicadas a aplicativos que usam as interfaces [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) ou [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) . Basta substituir **ISpatialAudioObjectRenderStream** nas etapas acima pelas interfaces Metadata ou HRTF.


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>
[Recuperando de um erro](recovering-from-an-invalid-device-error.md) 
 de Invalid-Device [Gerenciamento de fluxo](stream-management.md)
</dt> </dl>

 

 



