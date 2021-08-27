---
description: Saiba mais sobre notificações para roteamento de fluxo. As APIs implementam o roteamento de fluxo manipulando a troca de fluxo para um novo ponto de extremidade de áudio padrão.
ms.assetid: caf831bb-b8de-467f-bdb4-f9f8991dc7a8
title: Notificações relevantes para roteamento de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0660735590853161395b1cf771ba17bbb72e48e072b2f9daa11a0841c9a5c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109456"
---
# <a name="relevant-notifications-for-stream-routing"></a>Notificações relevantes para roteamento de fluxo

No Windows 7, as APIs de plataforma de alto nível que usam APIs de áudio principais, como as APIs Media Foundation, DirectSound e Wave, implementam o recurso de roteamento de fluxo manipulando a troca de fluxo de um dispositivo existente para um novo ponto de extremidade de áudio padrão. Os aplicativos de mídia que usam essas APIs usam o comportamento de roteamento de fluxo sem modificações na origem. Os clientes WASAPI diretos podem usar as notificações enviadas pelos componentes do Core Audio e implementar o recurso de roteamento de fluxo.

Para implementar o recurso de roteamento de fluxo, um cliente deve escutar dois tipos de eventos: notificações de alteração de dispositivo e notificações de desconexão de sessão. Na implementação fornecida pelas APIs de alto nível, esses eventos são enviados para pontos de extremidade de dispositivo padrão criados chamando [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Para obter mais informações, consulte [Getting the Device Endpoint for Stream Routing](getting-the-default-device-endpoint-for-stream-routing.md).

O componente áudio principal MMDeviceAPI fornece retornos de chamada de notificação quando os dispositivos de áudio são adicionados, removidos ou modificados. As alterações de formato e de sessão de áudio são relatadas como eventos por meio de WASAPI.

## <a name="device-change-notifications"></a>Notificações de alteração de dispositivo

MMDeviceAPI gera eventos quando os dispositivos de áudio são adicionados, removidos ou modificados. Se o cliente fornecer a funcionalidade de roteamento de fluxo, ele deverá implementar a interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e registrar sua implementação com MMDeviceAPI.

Para obter notificações de alteração do dispositivo, o cliente deve executar as seguintes tarefas:

-   Implemente a interface [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) para lidar com notificações de alteração de dispositivo enviadas por MMDeviceAPI.
-   Registre a implementação [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) com MMDeviceAPI chamando o método [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback)

Depois que a implementação dessas interfaces pelo cliente é registrada, o cliente recebe notificações na forma de retornos de chamada por meio dos métodos dessas interfaces. Os métodos [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) são chamados por MMDeviceAPI quando ele gera eventos no nível do ponto de extremidade (alterações de estado do ponto de extremidade, novas chegadas de ponto de extremidade, exclusões de ponto de extremidade, alterações de ponto de extremidade padrão e alterações de propriedade do ponto de extremidade).

Se o cliente quiser fornecer roteamento de fluxo para o dispositivo padrão, o cliente deverá implementar o comportamento de alteração do dispositivo quando receber a notificação por meio do retorno de chamada [**IMMNotificationClient::OnDefaultDeviceChanged.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged)

## <a name="audio-session-change-notifications"></a>Notificações de alteração de sessão de áudio

Alterações de sessão de áudio e alterações de formato são relatadas como eventos de sessão de áudio por meio de WASAPI. Um cliente WASAPI implementa a interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e registra a implementação com WASAPI.

Para obter notificações de alteração de sessão de áudio, o cliente deve executar as seguintes tarefas:

-   Implemente a interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) para manipular notificações de alteração de formato enviadas pelo WASAPI.
-   Registre a [**implementação de IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) com WASAPI chamando o [**método IAudioSessionControl::RegisterAudioSessionNotification.**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification)

[**Os métodos IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) são chamados pelo WASAPI quando ocorrem alterações de sessão de áudio. Esses eventos são gerados quando o nome de exibição da sessão, o caminho do ícone, o volume, o parâmetro de agrupação ou o estado da sessão são alterações.

Para implementar o recurso de roteamento de fluxo, o cliente deve aguardar a notificação de desconexão da sessão. Quando uma sessão de áudio é desconectada ou o formato de um dispositivo é alterado, o WASAPI envia as notificações do cliente na forma de retornos de chamada por [**meio de IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Com a notificação de desconexão, o WASAPI também envia um valor que indica por que a sessão foi desconectada. Isso pode ocorrer por vários motivos, como o dispositivo foi removido, o servidor parado e assim por diante. Para ver a lista completa de motivos, consulte a enumeração **AudioSessionDisconnectReason definida** em AudioPolicy.h. Se o dispositivo padrão mudar, o cliente deverá aguardar as notificações (se elas ainda não foram recebidas) que são acompanhadas com um valor **DisconnectReasonDeviceRemoval.** Em resposta a essas notificações, o cliente pode reabrir o fluxo no novo dispositivo padrão.

Como todas essas operações são assíncronas, a ordem na qual o aplicativo recebe notificações não pode ser prevista. No entanto, normalmente, o aplicativo recebe o **valor AudioSessionDisconnect** antes da notificação de alteração do dispositivo padrão.

### <a name="format-change-notifications"></a>Formatar notificações de alteração

As alterações de formato de áudio ocorrem quando o formato do fluxo muda. Isso pode ocorrer quando o usuário seleciona  um novo formato no painel de controle de som ou o novo dispositivo padrão dá suporte a um novo formato (por exemplo, HDMI ou determinadas interfaces de áudio profissionais com um ajuste manual de taxa de amostragem). Para notificar o cliente sobre esses tipos de alterações de formato, o WASAPI envia uma notificação de sessão pela implementação registrada [**de IAudioSessionEvents::OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) com um motivo de desconexão **de DisconnectReasonFormatChanged.** O cliente pode lidar com a notificação reabrindo o fluxo no novo formato.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API MMDevice](mmdevice-api.md)
</dt> <dt>

[Sobre WASAPI](wasapi.md)
</dt> <dt>

[Roteamento de fluxo](stream-routing.md)
</dt> </dl>

 

 



