---
description: Saiba mais sobre notificações para roteamento de fluxo. As APIs implementam o roteamento de fluxo manipulando a alternância de fluxo para um novo ponto de extremidade de áudio padrão.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Notificações relevantes para roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a843c1d8b5cfd740ada5049cb9428e7745072d
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068522"
---
# <a name="relevant-notifications-for-stream-routing"></a>Notificações relevantes para roteamento de fluxo

No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio de núcleo, como as APIs Media Foundation, DirectSound e Wave, implementam o recurso de roteamento de fluxo manipulando a alternância de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão. Os aplicativos de mídia que usam essas APIs usam o comportamento de roteamento de fluxo sem nenhuma modificação na origem. Os clientes Direct WASAPI podem usar as notificações enviadas pelos componentes de áudio principal e implementar o recurso de roteamento de fluxo.

Para implementar o recurso de roteamento de fluxo, um cliente deve escutar dois tipos de eventos: notificações de alteração de dispositivo e notificações de desconexão de sessão. Na implementação fornecida pelas APIs de alto nível, esses eventos são enviados para pontos de extremidade de dispositivo padrão criados chamando [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Para obter mais informações, consulte [obtendo o ponto de extremidade do dispositivo para roteamento de fluxo](getting-the-default-device-endpoint-for-stream-routing.md).

O componente de áudio principal MMDeviceAPI fornece retornos de chamada de notificação quando dispositivos de áudio são adicionados, removidos ou modificados. As alterações de sessão de formato e áudio são relatadas como eventos por meio de WASAPI.

## <a name="device-change-notifications"></a>Notificações de alteração do dispositivo

O MMDeviceAPI gera eventos quando os dispositivos de áudio são adicionados, removidos ou modificados. Se o cliente for fornecer a funcionalidade de roteamento de fluxo, ele deverá implementar a interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e registrar sua implementação com MMDeviceAPI.

Para obter notificações de alteração do dispositivo, o cliente deve executar as seguintes tarefas:

-   Implemente a interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) para lidar com notificações de alteração de dispositivo enviadas pelo MMDeviceAPI.
-   Registre a implementação de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) com MMDeviceAPI chamando o método [**IMMDeviceEnumerator:: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .

Depois que a implementação do cliente dessas interfaces é registrada, o cliente recebe notificações na forma de retornos de chamada por meio dos métodos dessas interfaces. Os métodos [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) são chamados por MMDeviceAPI quando gera eventos de nível de ponto de extremidade (alterações de estado do ponto de extremidade, novas entradas de ponto de extremidade, exclusões de ponto de extremidade, alterações de ponto de extremidade padrão e alterações de propriedade de ponto de extremidade)

Se o cliente quiser fornecer roteamento de fluxo para o dispositivo padrão, o cliente deverá implementar o comportamento de alteração do dispositivo quando receber a notificação por meio do retorno de chamada [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) .

## <a name="audio-session-change-notifications"></a>Notificações de alteração de sessão de áudio

Alterações de sessão de áudio e alterações de formato são relatadas como eventos de sessão de áudio por meio de WASAPI. Um cliente WASAPI implementa a interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e registra a implementação com WASAPI.

Para obter notificações de alteração de sessão de áudio, o cliente deve executar as seguintes tarefas:

-   Implemente a interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para lidar com notificações de alteração de formato enviadas pelo WASAPI.
-   Registre a implementação de [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) com WASAPI chamando o método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) .

Os métodos [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) são chamados por WASAPI quando ocorrem alterações na sessão de áudio. Esses eventos são gerados quando o nome de exibição da sessão, o caminho do ícone, o volume, o parâmetro de agrupamento ou as alterações de estado.

Para implementar o recurso de roteamento de fluxo, o cliente deve aguardar a notificação de desconexão de sessão. Quando uma sessão de áudio é desconectada ou o formato de um dispositivo é alterado, o WASAPI envia as notificações do cliente na forma de retornos de chamada por meio de [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Com a notificação de desconexão, o WASAPI também envia um valor que indica por que a sessão foi desconectada. Isso pode ocorrer por vários motivos, como o dispositivo foi removido, o servidor parou e assim por diante. Para obter a lista completa de motivos, consulte a enumeração **AudioSessionDisconnectReason** definida em AudioPolicy. h. Se o dispositivo padrão for alterado, o cliente deverá aguardar as notificações (se elas ainda não tiverem sido recebidas) que acompanham um valor **DisconnectReasonDeviceRemoval** . Em resposta a tais notificações, o cliente pode reabrir o fluxo no novo dispositivo padrão.

Como todas essas operações são assíncrona, a ordem na qual o aplicativo recebe notificações não foi possível ser prevista. No entanto, normalmente, o aplicativo recebe o valor de **AudioSessionDisconnect** antes da notificação de alteração de dispositivo padrão.

### <a name="format-change-notifications"></a>Notificações de alteração de formato

As alterações no formato de áudio ocorrem quando o formato do fluxo é alterado. Isso pode ocorrer quando o usuário seleciona um novo formato no painel de controle de **som** ou o novo dispositivo padrão dá suporte a um novo formato (por exemplo, HDMI ou algumas interfaces de áudio Professional com um ajuste de taxa de amostra manual). Para notificar o cliente sobre esses tipos de alterações de formato, o WASAPI envia uma notificação de sessão pela implementação registrada de [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) com um motivo de desconexão de **DisconnectReasonFormatChanged**. O cliente pode manipular a notificação reabrendo o fluxo no novo formato.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API do MMDevice](mmdevice-api.md)
</dt> <dt>

[Sobre o WASAPI](wasapi.md)
</dt> <dt>

[Roteamento de fluxo](stream-routing.md)
</dt> </dl>

 

 



