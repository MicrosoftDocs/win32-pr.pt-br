---
description: Especifica características que um cliente pode atribuir a um fluxo de áudio durante a inicialização do fluxo.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: AUDCLNT_STREAMFLAGS_XXX constantes (Audiosessiontypes.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84817607092c179286f47eb35ef51f5e0f82d44211bcd2345ca3d27ee06b0e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407359"
---
# <a name="audclnt_streamflags_xxx-constants"></a>Constantes AUDCLNT \_ STREAMFLAGS \_ XXX

Especifica características que um cliente pode atribuir a um fluxo de áudio durante a inicialização do fluxo.



| Constante/valor                                                                                                                                                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_ FLUXOFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | O fluxo de áudio será membro de uma sessão de áudio entre processos. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_ FLUXOFLAGS \_ LOOPBACK**</dt> <dt>0x00020000</dt> </dl>                                                   | O fluxo de áudio operará no modo de loopback. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK**</dt> <dt>0x00040000</dt> </dl>                                    | O processamento do buffer de áudio pelo cliente será orientado por eventos. Para obter mais informações, consulte Comentários. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ NOPERSIST**</dt> <dt>0x00080000</dt> </dl>                                                | As configurações de volume e mudo para uma sessão de áudio não persistirão entre as reinicializações do aplicativo. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | Essa constante é nova no Windows 7. A taxa de exemplo do fluxo é ajustada para uma taxa especificada por um aplicativo. Para obter mais informações, consulte Comentários. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**</dt> <dt>0x80000000</dt> </dl>                                 | Um matriz de canais e um conversor de taxa de exemplo são inseridos conforme necessário para converter entre o formato descompactado fornecido para [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) e o formato de combinação do mecanismo de áudio.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_ QUALIDADE PADRÃO \_ DO \_ \_ SRC DO STREAMFLAGS**</dt> <dt>0X08000000</dt> </dl>                | Quando usado com **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**, um conversor de taxa de exemplo com melhor qualidade do que a conversão padrão, mas com um custo de desempenho mais alto, é usado. Isso deve ser usado se o áudio for, em última análise, destinado a ser ouvido por humanos, em vez de outros cenários, como a bomba de silêncio ou o populamento de um medidor.<br/> |



## <a name="remarks"></a>Comentários

O [**método IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) e a estrutura [**\_ \_ \_ PARAMS**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) DE ATIVAÇÃO DE ÁUDIO DIRECTX usam as constantes AUDCLNT \_ STREAMFLAGS \_ XXX.

O sinalizador AUDCLNT \_ STREAMFLAGS CROSSPROCESS indica que a sessão de áudio para o fluxo é uma \_ sessão entre processos. Uma sessão entre processos pode aceitar fluxos de mais de um processo. Se dois aplicativos em dois processos separados **chamarem IAudioClient::Initialize** com GUIDs de sessão idênticos e ambos os aplicativos definirem o sinalizador AUDCLNT \_ SHAREMODE CROSSPROCESS, o mecanismo de áudio atribuirá seus fluxos à mesma sessão entre \_ processos. Esse sinalizador substitui o comportamento padrão, que é atribuir o fluxo a uma sessão específica do processo em vez de uma sessão entre processos. O bit do sinalizador AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS é incompatível com o modo exclusivo. Para obter mais informações sobre sessões entre processos, consulte [Sessões de áudio.](audio-sessions.md)

O sinalizador AUDCLNT \_ STREAMFLAGS \_ LOOPBACK habilita a gravação de loopback. Na gravação de loopback, o mecanismo de áudio copia o fluxo de áudio que está sendo interpretado por um dispositivo de ponto de extremidade de renderização em um buffer de ponto de extremidade de áudio para que um [cliente WASAPI](wasapi.md) possa capturar o fluxo. Se esse sinalizador for definido, o **método IAudioClient::Initialize** tentará abrir um buffer de captura no dispositivo de renderização. Esse sinalizador é válido somente para um dispositivo de renderização e somente se a **chamada Inicializar** define o parâmetro *ShareMode* como AUDCLNT \_ SHAREMODE \_ SHARED. Caso **contrário, a chamada Inicializar** falhará. Se a chamada for bem-sucedida, o cliente poderá chamar o método [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) para obter uma interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) no dispositivo de renderização. Para obter mais informações, consulte [Gravação de loopback](loopback-recording.md).

O sinalizador AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK habilita o buffer orientado a eventos. Se um cliente definir esse sinalizador na chamada para **IAudioClient::Initialize** que inicializa um fluxo, o cliente deverá chamar subsequentemente o método [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) para fornecer um alçamento de evento para o fluxo. Depois que o fluxo for iniciado, o mecanismo de áudio sinaliza o alçamento de evento para notificar o cliente sempre que um buffer ficar pronto para o cliente processar. O WASAPI dá suporte ao buffer orientado a eventos para buffers de renderização e captura. Os fluxos de modo compartilhado e de modo exclusivo podem usar o buffer orientado a eventos. Para ver um exemplo de código que usa o sinalizador \_ EVENTCALLBACK AUDCLNT STREAMFLAGS, consulte \_ Modo exclusivo [Fluxos](exclusive-mode-streams.md).

O sinalizador AUDCLNT \_ STREAMFLAGS NOPERSIST desabilita a persistência das configurações de volume e mute para uma sessão que contém \_ fluxos de renderização. Por padrão, o nível de volume e o estado de mutação de uma sessão de renderização são persistentes entre as reinicializações do aplicativo. O nível de volume e o estado de mutação de uma sessão de captura nunca são persistentes. Para obter mais informações sobre a persistência de configurações de volume de sessão e mute, consulte [Sessões de áudio](audio-sessions.md).

O sinalizador AUDCLNT STREAMFLAGS RATEADJUST permite que um aplicativo receba uma referência à \_ \_ interface [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) usada para definir a taxa de amostra para o fluxo. Para obter um ponteiro para essa interace, um aplicativo deve inicializar o cliente de áudio com esse sinalizador e, em seguida, chamar [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) especificando o **identificador \_ IID IAudioClockAdjustment.** Para definir a nova taxa de exemplo, chame [**IAudioClockAdjustment::SetSampleRate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate). Esse sinalizador é válido somente para um dispositivo de renderização. Caso contrário, **a chamada GetService** falhará com o código de erro AUDCLNT \_ E WRONG \_ \_ ENDPOINT \_ TYPE. O aplicativo também deve definir o *parâmetro ShareMode* como AUDCLNT \_ SHAREMODE \_ SHARED durante a [**chamada Inicializar.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) **SetSampleRate falhará** se o cliente de áudio não estiver no modo compartilhado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Audiosessiontypes.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de áudio principais](core-audio-constants.md)
</dt> <dt>

[**IAudioCaptureClient Interface**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




