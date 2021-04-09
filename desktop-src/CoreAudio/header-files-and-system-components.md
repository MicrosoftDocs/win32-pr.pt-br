---
description: Arquivos de cabeçalho e componentes do sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Arquivos de cabeçalho e componentes do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089516"
---
# <a name="header-files-and-system-components"></a>Arquivos de cabeçalho e componentes do sistema

A tabela a seguir lista os arquivos de cabeçalho que contêm as definições de interface para os quatro componentes de áudio principais.



|                                              |                              |
|----------------------------------------------|------------------------------|
| Componente de áudio principal                         | Arquivo de cabeçalho                  |
| [API MMDevice](mmdevice-api.md)             | Mmdeviceapi. h                |
| [WASAPI](wasapi.md)                         | Audioclient. h, Audiopolicy. h |
| [API DeviceTopology](devicetopology-api.md) | Devicetopology. h             |
| [API EndpointVolume](endpointvolume-api.md) | Endpointvolume. h             |



 

Outro arquivo de cabeçalho, Audiosessiontypes. h, define constantes que são usadas pelo WASAPI. Esses arquivos de cabeçalho estão localizados no diretório% MSSdk% \\ include, em que% MSSdk% é o diretório raiz da instalação do SDK do Windows no seu computador.

Cada API na tabela anterior consiste em um conjunto de interfaces COM relacionadas. Como alguns aspectos do streaming de áudio dependem da baixa latência e da sincronização precisa, as implementações das APIs MMDevice, WASAPI, DeviceTopology e EndpointVolume não usam o Microsoft .NET Framework ou o ambiente de execução gerenciada.

As APIs de áudio principais são implementadas nos componentes do sistema do modo de usuário Audioses.dll e Mmdevapi.dll. Os aplicativos cliente não acessam os pontos de entrada nessas DLLs diretamente. Em vez disso, os clientes chamam a função **CoCreateInstance** ou **CoCreateInstanceEx** para obter a interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) do objeto de classe MMDeviceEnumerator. Esse objeto enumera os [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema. A interface **IMMDeviceEnumerator** faz parte da API do MMDevice. A partir dessa interface, os clientes podem obter direta ou indiretamente as outras interfaces na API MMDevice, incluindo a interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . **IMMDevice** representa um dispositivo de ponto de extremidade de áudio específico. Por meio do **IMMDevice**, os clientes podem obter direta ou indiretamente as interfaces específicas do dispositivo em WASAPI, a API do DeviceTopology e a API do EndpointVolume. Para obter mais informações sobre **CoCreateInstance** e **CoCreateInstanceEx**, consulte a documentação do SDK do Windows. Para obter mais informações sobre como acessar as interfaces nas APIs de áudio principal, consulte [enumerando dispositivos de áudio](enumerating-audio-devices.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre as APIs de áudio do Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



