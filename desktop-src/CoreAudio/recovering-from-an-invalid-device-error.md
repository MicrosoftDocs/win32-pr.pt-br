---
description: Recuperando de um erro de Invalid-Device
ms.assetid: 1f5c3458-70ca-45ba-ac33-5c7b9f092320
title: Recuperando de um erro de Invalid-Device
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9f56972aeeae5cfb370a656a621c6b6e206f8caa115bec33203cab7eded3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318556"
---
# <a name="recovering-from-an-invalid-device-error"></a>Recuperando de um erro de Invalid-Device

Muitos dos métodos em WASAPI retornam o código de erro AUDCLNT \_ E \_ \_ o dispositivo invalidado se o dispositivo de ponto de extremidade de áudio que o aplicativo cliente está usando se tornar inválido. Esse código de erro indica que o dispositivo de ponto de extremidade foi desconectado ou que o hardware de áudio ou os recursos de hardware associados foram reconfigurados, desabilitados, removidos ou tornados de outra forma indisponíveis para uso. Frequentemente, o aplicativo pode se recuperar desse erro.

>[!NOTE]
> Para obter informações sobre a recuperação de erros de dispositivo inválidos ao usar ISAC (APIs de áudio espacial), consulte [recuperando de um erro de Invalid-Device (som espacial)](recovering-from-an-invalid-device-error-spatial-sound.md)

A estratégia que um aplicativo deve usar para se recuperar de um \_ \_ \_ erro invalidado do dispositivo AUDCLNT E depende de quais das técnicas a seguir o aplicativo usa para selecionar um dispositivo de ponto de extremidade de áudio:

-   Sempre selecione o dispositivo de captura ou processamento de áudio padrão.
-   Selecione um dispositivo de ponto de extremidade de áudio específico.

No último caso, o aplicativo seleciona automaticamente um dispositivo específico com base nos requisitos internos ou permite que o usuário selecione explicitamente um dispositivo de uma lista de dispositivos disponíveis.

Um aplicativo que usa o dispositivo padrão pode tentar se recuperar de um \_ \_ \_ erro invalidado do dispositivo AUDCLNT E, da seguinte maneira:

1.  Libere a interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e quaisquer outras interfaces WASAPI que ele tenha adquirido no dispositivo.
2.  Chame o método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter o dispositivo de áudio padrão atual.
3.  Tentativa de ativar o [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) no dispositivo de áudio padrão.

Seguindo as etapas anteriores, o aplicativo tende a responder adequadamente, independentemente da causa do \_ \_ \_ erro invalidado do dispositivo AUDCLNT E. Se a reconfiguração do dispositivo padrão tiver causado o erro (por exemplo, se o usuário alterou o formato de fluxo usado pelo dispositivo), essas etapas, se tiverem sucesso, permitirão que o aplicativo continue a usar o mesmo dispositivo. Se o usuário tiver desabilitado ou removido o dispositivo que o aplicativo estava usando e outro dispositivo estiver disponível para assumir a função do dispositivo padrão, o aplicativo poderá continuar usando o novo dispositivo padrão. Em ambos os casos, o aplicativo se adapta automaticamente sem a necessidade de intervenção pelo usuário.

Um aplicativo que seleciona um dispositivo específico pode tentar se recuperar do \_ \_ \_ erro invalidado do dispositivo AUDCLNT E, da seguinte maneira:

1.  Libere a interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) e quaisquer outras interfaces WASAPI que ele tenha adquirido no dispositivo.
2.  Tentativa de ativar uma interface [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) no mesmo dispositivo.
3.  Se a etapa 2 falhar, o aplicativo poderá, como opção, solicitar que o usuário selecione outro dispositivo.

A etapa 2 pode ter êxito se o dispositivo que está sendo usado pelo aplicativo tiver sido reconfigurado, mas não estiver desabilitado ou removido. Se for bem-sucedido, a etapa 2 permitirá que o aplicativo continue a usar automaticamente o mesmo dispositivo sem exigir a intervenção do usuário. A etapa 3 é apropriada se o aplicativo permitir que o usuário selecione explicitamente outro dispositivo depois que o usuário tiver desabilitado ou removido o dispositivo usado anteriormente.

Um aplicativo pode determinar mais precisamente a causa de um erro de dispositivo inválido ao se registrar para receber uma notificação quando uma sessão perde sua conexão com um dispositivo. Para habilitar essa notificação, o aplicativo implementa uma interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e chama o método [**IAudioSessionControl:: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) para registrar a interface. Quando um erro de dispositivo inválido faz com que a sessão seja desconectada, WASAPI chama o método [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) na interface registrada. Com esse método, o WASAPI informa o aplicativo do motivo da desconexão. no Windows Vista, a chamada **OnSessionDisconnected** identifica os seguintes motivos:

-   O usuário removeu o dispositivo de ponto de extremidade de áudio.
-   o serviço de áudio Windows foi desligado.
-   O formato de fluxo preferencial foi alterado para o dispositivo ao qual a sessão de áudio está conectada.
-   o usuário fez logoff da sessão de serviços de Terminal do Windows (WTS) na qual a sessão de áudio estava sendo executada. para obter mais informações sobre WTS sessões, consulte a documentação do SDK do Windows.
-   a sessão de WTS em que a sessão de áudio estava sendo executada foi desconectada.
-   A sessão de áudio (modo compartilhado) foi desconectada para tornar o dispositivo de ponto de extremidade de áudio disponível para uma conexão de modo exclusivo.

Em resposta ao evento de desconexão, WASAPI fecha todos os fluxos que pertencem à sessão. Se, posteriormente, um aplicativo tentar acessar um fluxo fechado por meio de um método WASAPI, como [**IAudioClient:: GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding), o método falhará e retornará o código de erro AUDCLNT \_ E o \_ dispositivo \_ invalidado.

Um benefício adicional para receber notificações por meio da interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) é que as notificações chegam de forma assíncrona. Portanto, mesmo quando o fluxo não está em execução, o aplicativo ainda receberá uma notificação oportuna de erros de dispositivo inválido que pode impedir a execução do fluxo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de fluxo](stream-management.md)
</dt> </dl>

 

 



