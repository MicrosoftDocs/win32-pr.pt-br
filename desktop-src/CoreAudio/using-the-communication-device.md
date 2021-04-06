---
description: No Windows 7, o painel de controle multimídia do Windows, Mmsys.cpl, fornece uma nova guia de comunicações.
ms.assetid: bec2127d-fb82-436d-beee-d43e8fef5c35
title: Usando um dispositivo de comunicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f677245e650cf11c71c879b2c26d3183ff4a0b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826475"
---
# <a name="using-a-communication-device"></a>Usando um dispositivo de comunicação

No Windows 7, o painel de controle multimídia do Windows, Mmsys.cpl, fornece uma nova guia de **comunicações** . Essa guia contém opções que permitem que um usuário defina opções que definem como o sistema gerencia um *dispositivo de comunicação*. Um dispositivo de comunicação é usado principalmente para colocar ou receber chamadas telefônicas no computador. Para um computador que tem apenas um dispositivo de renderização (alto-falante) e um dispositivo de captura (microfone), esses dispositivos de áudio também agem como os dispositivos de comunicação padrão. Quando um usuário conecta um novo dispositivo, como um headset USB, o sistema executa a detecção de função de dispositivo automática consultando as definições de configuração que são preenchidas pelo OEM. Se o sistema determinar que um dispositivo seja mais adequado para fins de comunicação, o sistema atribuirá a função **eCommunications** ao dispositivo. Para esses dispositivos, o Mmsys.cpl do Windows 7 fornece a opção **dispositivo de comunicação padrão** que permite que um usuário selecione um dispositivo de comunicação para a renderização de áudio (guia **reprodução** ) e captura de áudio (guia **gravação** ). O sistema executa a detecção automática de função, mas não define um dispositivo específico a ser usado para comunicações. Isso deve ser feito pelo usuário. A nova função **eCommunications** permite que um aplicativo diferencie um dispositivo escolhido pelo usuário para lidar com chamadas telefônicas e um dispositivo a ser usado como um dispositivo de multimídia (reprodução de música). Por exemplo, se o usuário tiver um headset e um palestrante conectado ao computador, o sistema atribuirá a função **eConsole** ao palestrante e à função **eCommunications** para o headset. Depois que o usuário selecionar o headset a ser usado como o dispositivo de comunicação, para desenvolver um aplicativo de comunicação, você poderá direcionar o headset especificamente para renderizar um fluxo de áudio. Um aplicativo que o usuário não pode alterar a função de dispositivo atribuída pelo sistema. Para obter mais informações sobre as funções de dispositivo, consulte [funções de dispositivo](device-roles.md).

Aplicativos de comunicação, como VoIP e aplicativos de comunicação unificada, colocam e recebem chamadas telefônicas por meio de um computador. Por exemplo, um aplicativo VoIP pode atribuir um fluxo que contém a notificação de toque para o ponto de extremidade de um conjunto de dispositivos de comunicação para renderização de fluxos de áudio. Além disso, o aplicativo pode abrir os fluxos de entrada e saída de voz nos dispositivos de ponto de extremidade de captura e renderização definidos como dispositivos de comunicação.

Para integrar os recursos de comunicação em seus aplicativos, você pode usar:

-   [API MMDevice](mmdevice-api.md)– para obter uma referência ao ponto de extremidade do dispositivo de comunicação.
-   [WASAPI](wasapi.md)— para renderizar e capturar fluxos de áudio por meio do dispositivo de comunicação. O sistema operacional considera o fluxo aberto em um dispositivo de comunicação como um *fluxo de comunicação*.

O aplicativo de comunicação enumera dispositivos e fornece gerenciamento de fluxo para um fluxo de fluxo de comunicação (renderização ou captura) da mesma maneira como ele gerenciaria um fluxo de não comunicação usando as APIs de áudio principais.

Um dos recursos que você pode integrar em seu aplicativo de comunicação é o *patoing* ou a *atenuação de fluxo*. Esse comportamento define o que deve acontecer com outros sons quando um fluxo de comunicação é aberto, por exemplo, quando uma chamada telefônica é recebida no dispositivo de comunicação. O sistema pode desativar ou reduzir o volume de áudio do fluxo de não comunicação, dependendo da escolha do usuário. O sistema de áudio gera eventos de pato quando um fluxo de comunicação é aberto ou fechado para renderização ou captura de fluxos. Por padrão, o sistema operacional fornece uma experiência de pato padrão. Um aplicativo de mídia pode substituir o comportamento padrão e lidar com esses eventos para fornecer uma experiência personalizada de pato.

As seções a seguir descrevem como usar as APIs de áudio de núcleo para fornecer uma experiência personalizada de pato.

-   [Experiência de pato padrão](stream-attenuation.md)
-   [Desabilitando a experiência de pato padrão](disabling-the-ducking-experience.md)
-   [Fornecendo um comportamento personalizado de pato](providing-a-custom-ducking-experience.md)
-   [Considerações de implementação para notificações de pato](handling-audio-ducking-events-from-communication-devices.md)
-   [Obtendo eventos de pato](getting-ducking-events-from-a-communication-device.md)

### <a name="getting-a-reference-to-the-communication-device-endpoint"></a>Obtendo uma referência para o ponto de extremidade do dispositivo de comunicação

Para usar o dispositivo de comunicação, um cliente WASAPI direto deve enumerar os dispositivos usando o enumerador de dispositivo. Obtenha uma referência para o ponto de extremidade do dispositivo de comunicação padrão chamando [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Nesta chamada, o aplicativo deve especificar **eCommunications** no parâmetro de *função* para restringir a enumeração do dispositivo a dispositivos de comunicação. Depois de obter uma referência ao ponto de extremidade do dispositivo para o dispositivo, você pode ativar os serviços que têm o escopo definido para o ponto de extremidade chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Por exemplo, você pode passar o identificador de serviço **\_ IAudioClient de IID** para ativar um objeto de cliente de áudio e usá-lo para o gerenciamento de fluxo, o identificador **\_ IAudioEndpointVolume de IID** para obter acesso aos controles de volume do ponto de extremidade do dispositivo de comunicação ou o identificador **\_ IAudioSessionManager do IID** para ativar o Gerenciador de sessão que permite que você interaja com o mecanismo de política do ponto de extremidade. Para obter informações sobre operações de fluxo, consulte [Gerenciamento de fluxo](stream-management.md).

Usando a referência [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , você também pode acessar o repositório de propriedades para o ponto de extremidade do dispositivo. Esses valores de propriedade, como nome amigável do dispositivo e nome do fabricante, são preenchidos pelo OEM e permitem que um aplicativo determine as características de um dispositivo de comunicação. Para obter mais informações, consulte [Propriedades do dispositivo](device-properties.md).

O código de exemplo a seguir obtém uma referência ao ponto de extremidade do dispositivo de comunicação padrão para renderizar um fluxo de áudio.


```C++
IMMDevice *defaultDevice = NULL;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), NULL,
            CLSCTX_INPROC_SERVER, 
            __uuidof(IMMDeviceEnumerator), 
            (LPVOID *)&deviceEnumerator);

hr = deviceEnumerator->GetDefaultAudioEndpoint(eRender, 
            eCommunications, &defaultDevice);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de fluxo](stream-management.md)
</dt> </dl>

 

 



