---
description: as APIs de áudio principais foram introduzidas no Windows Vista, que forneciam um novo conjunto de componentes de áudio no modo de usuário que um aplicativo cliente pode usar para renderizar ou capturar fluxos de áudio com recursos de áudio aprimorados.
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: o que há de novo para as APIs de áudio de núcleo no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6160b275512a7efbd3b795e263f2ce8ae01be965
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474702"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>o que há de novo para as APIs de áudio de núcleo no Windows 7

as APIs de áudio principais foram introduzidas no Windows Vista, que forneciam um novo conjunto de componentes de áudio no modo de usuário que um aplicativo cliente pode usar para renderizar ou capturar fluxos de áudio com recursos de áudio aprimorados. para obter uma visão geral desse conjunto de apis, consulte [sobre as APIs de áudio do Windows Core](about-the-windows-core-audio-apis.md).

as APIs de áudio principais foram aprimoradas no Windows 7. A tabela a seguir resume os novos recursos e as melhorias para as principais APIs de áudio:




| Recurso | Descrição | 
|---------|-------------|
| Aprimoramentos genéricos | os seguintes recursos foram aprimorados no Windows 7:<ul><li>em Windows 7 fluxos de modo de compartilhamento são executados em <em>modo de baixa latência</em>. O mecanismo de áudio é executado no modo de pull com uma redução significativa na latência. Isso é muito útil para aplicativos de comunicação que exigem baixa latência de fluxo de áudio para streaming mais rápido.</li><li>o Windows 7 fornece uma melhor detecção de função de dispositivo quando um novo dispositivo é adicionado ao sistema. Para obter mais informações, consulte <a href="device-roles-in-windows-vista.md">trabalhando com funções de dispositivo</a>.</li><li>no Windows 7, você pode ouvir música do seu player de mídia portátil por meio dos alto-falantes do computador. Você pode usar esse recurso de monitor de captura conectando um player de mídia portátil ao seu computador com um cabo de áudio analógico. No passado, alguns OEMs forneceram essa funcionalidade no driver de áudio usando um auto-retorno de hardware. no Windows 7, essa funcionalidade foi adicionada ao sistema operacional. Como isso está no sistema e não no driver, você pode usá-lo para qualquer outro dispositivo conectado ao sistema, como um headset USB.</li><li>o áudio HDMI foi aprimorado no Windows 7, que fornece suporte para o formato de alta taxa de bits. Com essa melhoria, você pode dar suporte a áudio multicanal e formatos de áudio compactados em um conector HDMI para um receptor de áudio.</li><li>no Windows Vista, Windows Media Player reproduz música somente por meio do dispositivo de áudio padrão, que não pode ser alterado pelo usuário. para Windows Media Player processar áudio para um dispositivo específico, o dispositivo padrão deve ser alterado no painel de controle <strong>sons</strong> . no Windows 7, Windows Media Player fornece APIs que permitem que um aplicativo seja renderizado em qualquer dispositivo selecionado pelo usuário e não apenas no dispositivo padrão.</li><li>no Windows Vista, se um computador que está reproduzindo comutador de áudio para o modo de economia de energia, o computador estiver bloqueado e se o usuário quiser interromper a reprodução, o usuário deverá fazer logon e pressionar a tecla stop para interromper a reprodução. no Windows 7, se o computador estiver bloqueado, você ainda poderá controlar a reprodução usando o controle HID no teclado.</li><li>o Windows 7 reduz o consumo de energia para qualquer aplicativo que usa DirectSound e DirectShow para renderizar mídia. Além disso, o serviço de Agendador de classes de multimídia permite áudio resistente a falhas e usa menos energia enquanto os exemplos de áudio estão sendo gerados.</li></ul> | 
| Dispositivo de comunicação (novo) | Nesta versão, um novo tipo de dispositivo foi adicionado ao painel de controle <strong>sons</strong> : dispositivo de <strong>comunicações</strong> . Esse dispositivo é usado principalmente para comunicações, ou seja, para fazer ou receber chamadas telefônicas no computador. Um aplicativo de comunicação pode usar os principais componentes de áudio para obter uma referência ao ponto de extremidade do dispositivo de comunicação padrão e renderizar fluxos de áudio para fins de comunicação. O sistema operacional considera o fluxo aberto em um dispositivo de comunicação como um fluxo de comunicação. As operações WASAPI em um fluxo de comunicação são semelhantes a qualquer outro fluxo de áudio. Para obter mais informações, consulte <a href="device-roles-in-windows-vista.md">trabalhando com funções de dispositivo</a>. | 
| Atenuação de fluxo ou o pato de áudio (novo) | o pato automático ou a <a href="stream-attenuation.md">atenuação de fluxo</a> é um novo recurso do Windows 7 destinado a aplicativos de comunicação unificada e VoIP. Por padrão, o sistema operacional reduz a intensidade de um fluxo de áudio quando um fluxo de comunicação, como uma chamada telefônica, é recebido no dispositivo de comunicação por meio do computador. As opções de volume são definidas pelo usuário no painel de controle de <strong>som</strong> . novas APIs foram adicionadas no SDK do Windows que permitem que os aplicativos substituam o comportamento de pato padrão. Para obter mais informações sobre como implementar um recurso de pato personalizado, consulte <a href="providing-a-custom-ducking-experience.md">fornecendo um comportamento de patoing personalizado</a>. <br /> | 
| Roteamento de fluxo (novo) | no Windows 7, as APIs de áudio principais foram aprimoradas para transferir um fluxo de áudio diretamente de um dispositivo existente para um novo ponto de extremidade de áudio padrão. Conjuntos de API de áudio de alto nível que usam APIs de áudio de núcleo, como as APIs Media Foundation, DirectSound e WAVE, implementam o recurso de roteamento de fluxo. Os aplicativos de mídia que usam esses conjuntos de API para reproduzir ou capturar um fluxo usam a implementação padrão e não precisam modificar o aplicativo. No entanto, se o aplicativo de mídia usar APIs de áudio de núcleo diretamente, o aplicativo precisará fornecer a implementação de roteamento de fluxo. Para fazer isso, o aplicativo deve manipular novos eventos que foram adicionados para notificar um cliente WASAPI quando o dispositivo padrão é conectado ou removido. Para obter mais informações sobre esse recurso, consulte <a href="stream-routing.md">Roteamento de fluxo</a>. | 
| Áudio do modo de usuário protegido (PUMA) (aprimorado) | o PUMA foi atualizado para o Windows 7 para fornecer os seguintes recursos:<ul><li>Definir bits SCMS (sistema de gerenciamento de cópia serial) em pontos de extremidade S/PDIF e bits de Proteção de Conteúdo Digital de largura de banda alta (HDCP) em pontos de extremidade de HDMI (High-Definition Multimedia Interface).</li><li>Habilitando controles de proteção SCMS e HDMI fora de um ambiente protegido (PE).</li></ul>Para obter mais informações sobre as melhorias, consulte <a href="protected-user-mode-audio--puma-.md">áudio do modo de usuário protegido (Puma)</a>.<br /> | 
| A estrutura <strong>WAVEFORMATEXTENSIBLE</strong> foi estendida para a estrutura de <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> (nova) | no Windows 7, uma nova estrutura foi adicionada para dar suporte a transmissões IEC 61937. <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> estende a estrutura <strong>WAVEFORMATEXTENSIBLE</strong> para armazenar dois conjuntos de características de fluxo de áudio: o formato de áudio codificado antes da transmissão e das características do fluxo de áudio depois que ele é decodificado. A nova estrutura especifica explicitamente o número efetivo de canais, o tamanho da amostra e a taxa de dados de um formato não PCM. Com essas informações, um aplicativo pode inferir o nível de qualidade do fluxo não PCM depois de ser descompactado e reproduzido. Para obter mais informações, consulte <a href="representing-formats-for-iec-61937-transmissions.md">representando formatos para transmissões IEC 61937</a>.<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a> (aprimorado) | O método <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a> foi aprimorado para indicar erros específicos que podem ocorrer durante a abertura de um fluxo de áudio. Os novos códigos de erro são:<ul><li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li><li>AUDCLNT_E_BUFFER_SIZE_ERROR</li><li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li></ul>Para obter mais informações sobre esses erros, consulte a seção valor de retorno em <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: GetBuffer</strong></a> (aprimorado) | Os métodos <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: GetBuffer</strong></a> foram aprimorados para retornar o AUDCLNT_E_BUFFER_ERROR código de erro que indica que o buffer de ponto de extremidade no modo exclusivo não foi recuperado. Para obter mais informações, consulte comentários em <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: GetBuffer</strong></a>. | 
| Capacidade de detecção de tomada (aprimorada) | uma nova interface no Windows 7, <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2</strong></a>, estende <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>IKsJackDescription</strong></a>. Usando a nova interface, a pilha de áudio ou um aplicativo pode obter informações adicionais sobre a Jack. Isso inclui a capacidade de detecção da tomada e se o formato do dispositivo foi alterado dinamicamente. | 
| Windows Exemplos (novo) | novos exemplos foram adicionados à SDK do Windows que demonstram o uso das APIs de áudio principais. Para obter mais informações, consulte <a href="sdk-samples-that-use-the-core-audio-apis.md">exemplos de SDK que usam as APIs de áudio de núcleo</a>. | 




 

## <a name="major-new-interfaces"></a>Principais novas interfaces

as seguintes interfaces são novas para o Windows 7:

-   [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)
-   [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)
-   [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)
-   [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)
-   [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)
-   [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)
-   [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)
-   [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)
-   [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)
-   [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[sobre as APIs de áudio do Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




