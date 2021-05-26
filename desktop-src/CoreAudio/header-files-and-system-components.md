---
description: Arquivos de header e componentes do sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Arquivos de header e componentes do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a47125853b51a71f2f05dacf4534ce33cfedec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424286"
---
# <a name="header-files-and-system-components"></a>Arquivos de header e componentes do sistema

A tabela a seguir lista os arquivos de header que contêm as definições de interface para os quatro componentes do Core Audio.



| Componente de áudio principal                         | Arquivo de cabeçalho                  |
|----------------------------------------------|------------------------------|
| [MMDevice API](mmdevice-api.md)             | Mmdeviceapi.h                |
| [WASAPI](wasapi.md)                         | Audioclient.h, Audiopolicy.h |
| [DeviceTopology API](devicetopology-api.md) | Devicetopology.h             |
| [EndpointVolume API](endpointvolume-api.md) | Endpointvolume.h             |



 

Outro arquivo de header, Audiosessiontypes.h, define constantes que são usadas pelo WASAPI. Esses arquivos de header estão localizados no diretório %MSSdk%, em que %MSSdk% é o diretório raiz da instalação \\ SDK do Windows no computador.

Cada API na tabela anterior consiste em um conjunto de interfaces COM relacionadas. Como alguns aspectos do streaming de áudio dependem de baixa latência e sincronização precisa, as implementações das APIs MMDevice, WASAPI, DeviceTopology e EndpointVolume não usam o Microsoft .NET Framework ou o ambiente de execução gerenciada.

As APIs de Áudio Principal são implementadas nos componentes do sistema de modo de usuário Audioses.dll e Mmdevapi.dll. Os aplicativos cliente não acessam os pontos de entrada nessas DLLs diretamente. Em vez disso, os clientes chamam a função **CoCreateInstance** ou **CoCreateInstanceEx** para obter a interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) do objeto de classe MMDeviceEnumerator. Esse objeto enumera os [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema. A interface **IMMDeviceEnumerator** faz parte da API do MMDevice. A partir dessa interface, os clientes podem obter direta ou indiretamente as outras interfaces na API MMDevice, incluindo a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . **IMMDevice** representa um dispositivo de ponto de extremidade de áudio específico. Por meio do **IMMDevice**, os clientes podem obter direta ou indiretamente as interfaces específicas do dispositivo em WASAPI, a API do DeviceTopology e a API do EndpointVolume. Para obter mais informações sobre **CoCreateInstance** e **CoCreateInstanceEx**, consulte a documentação do SDK do Windows. Para obter mais informações sobre como acessar as interfaces nas APIs de áudio principal, consulte [enumerando dispositivos de áudio](enumerating-audio-devices.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre as APIs de áudio do Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



