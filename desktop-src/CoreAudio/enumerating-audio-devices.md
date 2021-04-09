---
description: Enumerando dispositivos de áudio
ms.assetid: 20110ffc-5eff-4279-abea-53115803b6ee
title: Enumerando dispositivos de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707b9a88181c83344757c711af1c0199c19ebc16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010215"
---
# <a name="enumerating-audio-devices"></a>Enumerando dispositivos de áudio

A primeira tarefa de um aplicativo de áudio de cliente é encontrar um dispositivo de áudio adequado para uso. A [API MMDevice](mmdevice-api.md) permite que os clientes descubram os [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) no sistema e determine quais dispositivos são adequados para o aplicativo usar. Essa API permite que os clientes recuperem coleções dos dispositivos de ponto de extremidade disponíveis e obtenham os recursos de cada dispositivo. O arquivo de cabeçalho Mmdeviceapi. h define as interfaces na API MMDevice.

Um adaptador de áudio pode conter vários dispositivos — por exemplo, um dispositivo de processamento de ondas e um dispositivo de captura de onda. Esses são dispositivos de adaptador em vez de dispositivos de ponto de extremidade. Conforme mencionado anteriormente, os dispositivos de adaptador são registrados pelo Gerenciador de Plug and Play, em comparação com os dispositivos de ponto de extremidade, que são registrados pelo Gerenciador de pontos de extremidade. Normalmente, cada dispositivo de adaptador dá suporte a um ou mais dispositivos de ponto de extremidade. Um dispositivo de ponto de extremidade de renderização (por exemplo, fones de ouvido) pode receber um fluxo de dados de áudio de um aplicativo cliente e um dispositivo de ponto de extremidade de captura (por exemplo, um microfone) pode enviar um fluxo de áudio para um aplicativo cliente.

Antes de enumerar os dispositivos de ponto de extremidade no sistema, o cliente deve primeiro chamar a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) do Windows para criar um enumerador de dispositivo. Um enumerador de dispositivo é um objeto com uma interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Para obter informações sobre **CoCreateInstance**, consulte a documentação do SDK do Windows.

O cliente chama o método [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) para criar uma coleção de objetos de ponto de extremidade. Cada objeto de ponto de extremidade representa um dispositivo de ponto de extremidade de áudio no sistema. Nesta chamada, o cliente especifica se a coleção deve conter todos os dispositivos de renderização no sistema, todos os dispositivos de captura ou ambos.

Uma coleção de dispositivos é um objeto com uma interface [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . Cada item em uma coleção de dispositivos é um objeto de ponto de extremidade com pelo menos as duas interfaces a seguir:

-   Uma interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . Um cliente obtém uma referência à interface **IMMDevice** de um objeto de ponto de extremidade em uma coleção de dispositivos chamando o método [**IMMDeviceCollection:: item**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevicecollection-item) .
-   Uma interface [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint) . Um cliente obtém uma referência à interface **IMMEndpoint** de um objeto de ponto de extremidade chamando o método [**IMMDevice:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

Depois de recuperar uma coleção de dispositivos de ponto de extremidade, o cliente pode consultar as propriedades dos dispositivos individuais na coleção para determinar sua adequação para uso. Para obter um exemplo de código que mostra como enumerar dispositivos de ponto de extremidade e consultar suas propriedades, consulte [Propriedades do dispositivo](device-properties.md).

Depois de selecionar um dispositivo adequado, o cliente pode chamar o método [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para ativar as interfaces específicas do dispositivo no [WASAPI](wasapi.md), a [API do DeviceTopology](devicetopology-api.md)e a API do [EndpointVolume](endpointvolume-api.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md)
</dt> </dl>

 

 
