---
description: Enumerando dispositivos de áudio
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Enumerando dispositivos de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5d21ec2de2b08ca3c6f26884bd210b2f149caaa9e3b6a4402b69dde9fb7540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018374"
---
# <a name="enumerating-audio-devices"></a>Enumerando dispositivos de áudio

A primeira tarefa de um aplicativo de áudio cliente é encontrar um dispositivo de áudio adequado a ser usado. A [API MMDevice](mmdevice-api.md) permite [](audio-endpoint-devices.md) que os clientes descubram os dispositivos de ponto de extremidade de áudio no sistema e determinem quais dispositivos são adequados para o aplicativo usar. Essa API permite que os clientes recuperem coleções dos dispositivos de ponto de extremidade disponíveis e recebam os recursos de cada dispositivo. O arquivo de cabeça Mmdeviceapi.h define as interfaces na API MMDevice.

Um adaptador de áudio pode conter vários dispositivos, por exemplo, um dispositivo de renderização de onda e um dispositivo de captura de onda. Esses são dispositivos de adaptador em vez de dispositivos de ponto de extremidade. Conforme mencionado anteriormente, os dispositivos de adaptador são registrados pelo gerenciador Plug and Play, ao contrário dos dispositivos de ponto de extremidade, que são registrados pelo gerenciador de ponto de extremidade. Cada dispositivo de adaptador normalmente dá suporte a um ou mais dispositivos de ponto de extremidade. Um dispositivo de ponto de extremidade de renderização (por exemplo, fones de ouvido) pode receber um fluxo de dados de áudio de um aplicativo cliente e um dispositivo de ponto de extremidade de captura (por exemplo, um microfone) pode enviar um fluxo de áudio para um aplicativo cliente.

Antes de enumerar os dispositivos de ponto de extremidade no sistema, o cliente deve primeiro chamar a função [**Windows CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um enumerador de dispositivo. Um enumerador de dispositivo é um objeto com uma interface [**IMMDeviceEnumerator.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Para obter informações sobre **o CoCreateInstance,** consulte a documentação Windows SDK.

O cliente chama o [**método IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) para criar uma coleção de objetos de ponto de extremidade. Cada objeto de ponto de extremidade representa um dispositivo de ponto de extremidade de áudio no sistema. Nessa chamada, o cliente especifica se a coleção deve conter todos os dispositivos de renderização no sistema, todos os dispositivos de captura ou ambos.

Uma coleção de dispositivos é um objeto com uma interface [**IMMDeviceCollection.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) Cada item em uma coleção de dispositivos é um objeto de ponto de extremidade com pelo menos as duas interfaces a seguir:

-   Uma [**interface IMMDevice.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) Um cliente obtém uma referência à interface **IMMDevice** de um objeto de ponto de extremidade em uma coleção de dispositivos chamando o [**método IMMDeviceCollection::Item.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item)
-   Uma [**interface IMMEndpoint.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) Um cliente obtém uma referência à interface **IMMEndpoint** de um objeto de ponto de extremidade chamando o [**método IMMDevice::QueryInterface.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

Depois de recuperar uma coleção de dispositivos de ponto de extremidade, o cliente pode consultar as propriedades dos dispositivos individuais na coleção para determinar sua adequação para uso. Para ver um exemplo de código que mostra como enumerar dispositivos de ponto de extremidade e consultar suas propriedades, consulte [Propriedades do dispositivo](device-properties.md).

Depois de selecionar um dispositivo adequado, o cliente pode chamar o método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para ativar as interfaces específicas do dispositivo no [WASAPI,](wasapi.md)na [API DeviceTopology](devicetopology-api.md)e na [API endpointVolume.](endpointvolume-api.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> </dl>

 

 
