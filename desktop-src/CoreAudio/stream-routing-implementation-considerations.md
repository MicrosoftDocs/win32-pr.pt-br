---
description: Saiba mais sobre as considerações de implementação para roteamento de fluxo. As APIs implementam o roteamento de fluxo manipulando a alternação de fluxo para um novo ponto de extremidade de áudio padrão.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Considerações sobre implementação de roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bd753fe027c92ffac9f5a41cea589b600d7f26
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068032"
---
# <a name="stream-routing-implementation-considerations"></a>Considerações sobre implementação de roteamento de fluxo

No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio principais, como apIs de áudio Media Foundation, DirectSound e Wave, implementam o recurso de roteamento de fluxo manipulando a troca de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão. Os aplicativos de mídia que usam essas APIs usam o comportamento de roteamento de fluxo sem nenhuma modificação na origem. Os clientes WASAPI diretos podem usar as notificações enviadas pelos componentes do Core Audio e implementar o recurso de roteamento de fluxo.

Clientes WASAPI diretos (aplicativos de mídia que usam WASAPI diretamente) recebem novas notificações de dispositivo e de sessão de áudio enviadas pelos componentes do Core Audio. O comportamento do recurso de roteamento de fluxo é definido por como o aplicativo lida com essas notificações.

A API MMDevice e a sessão de áudio enviam notificações sobre alterações de estado do dispositivo e alterações de sessão para clientes WASAPI na forma de retornos de chamada. Para obter essas notificações, o cliente deve registrar sua implementação [**de IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents). Para obter mais informações, consulte [Notificações relevantes para roteamento de fluxo.](relevant-device-notifications-for-stream-routing.md)

No cenário de headset USB descrito em [Roteamento](stream-routing.md)de Fluxo, um aplicativo está tocando um fluxo de áudio e usa MMDeviceAPI e WASAPI para renderizar o fluxo no dispositivo de renderização padrão, o **Locutor**. Quando o dispositivo padrão é alterado, o aplicativo recebe uma [**notificação IMMNotificationClient.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) O aplicativo também recebe notificações [**de IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) indicando que o usuário removeu o dispositivo de ponto de extremidade de áudio ou que o formato de fluxo foi alterado para o dispositivo ao qual a sessão de áudio está conectada. Após receber as notificações, o aplicativo interrompe o streaming para o ponto de extremidade do locutor e reabre o fluxo para renderização no ponto de extremidade padrão atual, o headset.

![diagrama do fluxo de dados para notificações do dispositivo.](images/stream-routing.gif)

Em resposta a essas notificações, o cliente pode reabrir o fluxo no novo dispositivo padrão no novo formato selecionado pelo usuário.

## <a name="stream-managment"></a>Stream Managment

A lista a seguir resume as etapas que um cliente WASAPI deve executar para fornecer a funcionalidade de troca de fluxo.

1.  Aguarde a notificação [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) relevante. Se o dispositivo for o dispositivo padrão, a notificação [**IMMNotificationClient::OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) será recebida.
2.  Se um novo dispositivo estiver disponível, obter uma referência ao ponto de extremidade do novo dispositivo. Chame [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para o novo dispositivo padrão. Se o novo dispositivo não for o dispositivo padrão, você poderá recuperar o dispositivo chamando [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice). Para obter mais informações, consulte [Getting the Device Endpoint for Stream Routing](getting-the-default-device-endpoint-for-stream-routing.md).
3.  Aguarde o [**IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) com o valor do motivo.
    > [!Note]  
    > Como todas essas operações são assíncronas, a ordem na qual o aplicativo recebe notificações de alteração de dispositivo e desconexão de sessão não pode ser prevista. O aplicativo deve implementar o tratamento de notificação para receber essas notificações em qualquer ordem. No entanto, normalmente, o aplicativo recebe o **valor AudioSessionDisconnect** antes da notificação de alteração do dispositivo padrão.

     

4.  Avalie o valor do motivo e determine se o fluxo precisa ser transferido para outro ponto de extremidade de áudio ou se o fluxo precisa ser reinicializado com um novo formato.
5.  Pare o streaming para o dispositivo padrão antigo se o motivo indicar que o fluxo deve ser roteado para o novo dispositivo padrão.
6.  Executar cálculos de mapeamento de posição.
7.  Abra o fluxo no novo dispositivo e transfira todas as informações de estado.
8.  Retome o streaming no novo dispositivo padrão.
9.  Manipular a partida do dispositivo padrão antigo.

Para que a operação de alternação de fluxo pareça perfeita, ela deve ser feita o mais rápido possível. Isso depende do desempenho dos componentes envolvidos na re-inicialização do fluxo no novo dispositivo.

## <a name="position-mapping-considerations"></a>Considerações sobre mapeamento de posição

Quando o aplicativo obtém notificações [**de IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents,**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ele pode rotear os fluxos existentes para o novo dispositivo padrão. Quando um fluxo de áudio existente é interrompido e aberto no novo dispositivo, a renderização no novo dispositivo deve começar na posição em que o fluxo foi interrompido no dispositivo antigo. Para fazer isso, o aplicativo deve ter a última posição de dispositivo conhecida para calcular a posição inicial no novo dispositivo. Por exemplo, essa posição pode ser usada como o deslocamento delta para mapeamento de posição subsequente. Quando o fluxo inicia a renderização, a nova posição do dispositivo pode ser remapped para a posição do dispositivo armazenado em cache.

As etapas a seguir resumem o processo de fazer uma transição contínua de fluxo.

1.  Armazenar em cache a última posição do dispositivo do fluxo no dispositivo antigo.
2.  Pare o fluxo no dispositivo antigo.
3.  Execute cálculos de remapeamento para obter a nova posição.
4.  Comece a renderizar o fluxo no novo dispositivo.
5.  Libere o fluxo antigo.

Durante a transição, o aplicativo deve garantir que o relógio não saia da sincronização, resultando em fluxos de áudio e vídeo fora de sincronia. Isso pode ocorrer se os exemplos de vídeo continuarem a ser renderados enquanto o fluxo de áudio é roteado para o novo dispositivo. O aplicativo deve armazenar em cache a posição do relógio para o cálculo de remapeamento e garantir que os exemplos de vídeo não sejam renderizados até que o fluxo de áudio seja reaberto no novo dispositivo, para que, quando o clipe retomar a renderização, o áudio e os fluxos de vídeo sejam sincronizados. Em alguns casos, em que o tempo de apresentação para renderizar os quadros de vídeo é baseado no relógio de áudio, é suficiente interromper o fluxo de áudio até que a alternação de fluxo seja concluída e nenhuma outra implementação de mapeamento de posição para o fluxo de vídeo seja necessária para sincronização de vídeo de áudio.

Se, durante a renderização, [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) retornar um erro porque o dispositivo antigo foi perdido, o aplicativo não precisará interromper o fluxo antigo porque a operação de streaming já foi encerrada. Para obter informações sobre como tratar esse erro, consulte [Recuperando de um erro Invalid-Device erro](recovering-from-an-invalid-device-error.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API MMDevice](mmdevice-api.md)
</dt> <dt>

[Sobre WASAPI](wasapi.md)
</dt> <dt>

[Roteamento de fluxo](stream-routing.md)
</dt> </dl>

 

 



