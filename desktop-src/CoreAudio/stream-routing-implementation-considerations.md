---
description: No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio de núcleo, como as APIs Media Foundation, DirectSound e Wave, implementam o recurso de roteamento de fluxo manipulando a alternância de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Considerações de implementação de roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27dc1f7e3fe56d6b421ca59f528ab1a65d2261a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920404"
---
# <a name="stream-routing-implementation-considerations"></a>Considerações de implementação de roteamento de fluxo

No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio de núcleo, como as APIs Media Foundation, DirectSound e Wave, implementam o recurso de roteamento de fluxo manipulando a alternância de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão. Os aplicativos de mídia que usam essas APIs usam o comportamento de roteamento de fluxo sem nenhuma modificação na origem. Os clientes Direct WASAPI podem usar as notificações enviadas pelos componentes de áudio principal e implementar o recurso de roteamento de fluxo.

Os clientes Direct WASAPI (aplicativos de mídia que usam o WASAPI diretamente) recebem novas notificações de dispositivo e de sessão de áudio enviadas por componentes de áudio principais. O comportamento do recurso de roteamento de fluxo é definido por como o aplicativo manipula essas notificações.

A API MMDevice e a sessão de áudio enviam notificações sobre alterações de estado do dispositivo e alterações de sessão para clientes WASAPI na forma de retornos de chamada. Para obter essas notificações, o cliente deve registrar sua implementação de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents). Para obter mais informações, consulte [notificações relevantes para roteamento de fluxo](relevant-device-notifications-for-stream-routing.md).

No cenário de headset USB descrito em [Roteamento de fluxo](stream-routing.md), um aplicativo está reproduzindo um fluxo de áudio e usa MMDEVICEAPI e WASAPI para renderizar o fluxo no dispositivo de renderização padrão, no **palestrante**. Quando o dispositivo padrão é alterado, o aplicativo recebe uma notificação [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) . O aplicativo também recebe notificações [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) indicando que o usuário removeu o dispositivo de ponto de extremidade de áudio ou que o formato de fluxo foi alterado para o dispositivo ao qual a sessão de áudio está conectada. Após o recebimento das notificações, o aplicativo para de streaming para o ponto de extremidade do orador e reabre o fluxo para renderização no ponto de extremidade padrão atual, o headset.

![diagrama de fluxo de dados para notificações de dispositivo.](images/stream-routing.gif)

Em resposta a tais notificações, o cliente pode reabrir o fluxo no novo dispositivo padrão no novo formato selecionado pelo usuário.

## <a name="stream-managment"></a>Gerenciamento de fluxo

A lista a seguir resume as etapas que um cliente WASAPI deve executar para fornecer a funcionalidade de comutação de fluxo.

1.  Aguarde a notificação de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) relevante. Se o dispositivo for o dispositivo padrão, a notificação [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) será recebida.
2.  Se um novo dispositivo estiver disponível, obtenha uma referência para o ponto de extremidade do novo dispositivo. Chame [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para o novo dispositivo padrão. Se o novo dispositivo não for o dispositivo padrão, você poderá recuperar o dispositivo chamando [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice). Para obter mais informações, consulte [obtendo o ponto de extremidade do dispositivo para roteamento de fluxo](getting-the-default-device-endpoint-for-stream-routing.md).
3.  Aguarde o [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) com o valor do motivo.
    > [!Note]  
    > Como todas essas operações são assíncrona, a ordem na qual o aplicativo recebe notificações de alteração de dispositivo e de desconexão de sessão não foi possível ser prevista. O aplicativo deve implementar o tratamento de notificação para receber essas notificações em qualquer ordem. No entanto, normalmente, o aplicativo recebe o valor de **AudioSessionDisconnect** antes da notificação de alteração de dispositivo padrão.

     

4.  Avalie o valor do motivo e determine se o fluxo precisa ser transferido para outro ponto de extremidade de áudio ou se o fluxo precisa ser reinicializado com um novo formato.
5.  Pare o streaming para o dispositivo padrão antigo se o motivo indicar que o fluxo deve ser roteado novamente para o novo dispositivo padrão.
6.  Executar cálculos de mapeamento de posição.
7.  Abra o fluxo no novo dispositivo e transfira todas as informações de estado.
8.  Retomar streaming no novo dispositivo padrão.
9.  Manipule a saída do antigo dispositivo padrão.

Para fazer com que a operação de alternância de fluxo pareça direta, ela deve ser feita o mais rapidamente possível. Isso depende do desempenho dos componentes envolvidos na reinicialização do fluxo no novo dispositivo.

## <a name="position-mapping-considerations"></a>Considerações sobre mapeamento de posição

Quando o aplicativo obtém notificações [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) , ele pode rotear os fluxos existentes para o novo dispositivo padrão. Quando um fluxo de áudio existente é interrompido e aberto no novo dispositivo, a renderização no novo dispositivo deve começar na posição em que o fluxo foi interrompido no dispositivo antigo. Para fazer isso, o aplicativo deve ter a última posição de dispositivo conhecida para calcular a posição inicial no novo dispositivo. Por exemplo, essa posição pode ser usada como o deslocamento Delta para mapeamento de posição subsequente. Quando o fluxo inicia a renderização, a nova posição do dispositivo pode ser remapeada para a posição do dispositivo em cache.

As etapas a seguir resumem o processo de fazer uma transição de fluxo contínuo.

1.  Armazenar em cache a última posição do dispositivo do fluxo no dispositivo antigo.
2.  Pare o fluxo no dispositivo antigo.
3.  Execute remapeando cálculos para obter a nova posição.
4.  Comece a renderizar o fluxo no novo dispositivo.
5.  Libere o fluxo antigo.

Durante a transição, o aplicativo deve garantir que o relógio não seja sincronizado, resultando em fluxos de áudio e vídeo fora de sincronia. Isso pode ocorrer se os exemplos de vídeo continuarem a ser renderizados enquanto o fluxo de áudio é roteado para o novo dispositivo. O aplicativo deve armazenar em cache a posição do relógio para o cálculo do remapeamento e certificar-se de que os exemplos de vídeo não sejam renderizados até que o fluxo de áudio seja reaberto no novo dispositivo, para que, quando o clipe retomar a renderização, os fluxos de áudio e de vídeo sejam sincronizados. Em alguns casos, onde o tempo de apresentação para renderizar os quadros de vídeo é baseado no relógio de áudio, é suficiente parar o fluxo de áudio até que a alternância de fluxo seja concluída e nenhuma outra implementação de mapeamento de posição para o fluxo de vídeo é necessária para a sincronização de vídeo em áudio.

Se durante a renderização, [**IAudioRenderClient:: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) retornará um erro porque o dispositivo antigo é perdido, o aplicativo não precisa parar o fluxo antigo porque a operação de streaming já foi encerrada. Para obter informações sobre como lidar com esse erro, consulte [recuperando de um erro de Invalid-Device](recovering-from-an-invalid-device-error.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API do MMDevice](mmdevice-api.md)
</dt> <dt>

[Sobre o WASAPI](wasapi.md)
</dt> <dt>

[Roteamento de fluxo](stream-routing.md)
</dt> </dl>

 

 



