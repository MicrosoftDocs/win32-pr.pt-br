---
description: Especifica as características que um cliente pode atribuir a um fluxo de áudio durante a inicialização do fluxo.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: Constantes de AUDCLNT_STREAMFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65faf887c35b4ce1110cecb7d7509eb3dfda1d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089250"
---
# <a name="audclnt_streamflags_xxx-constants"></a>\_Constantes AUDCLNT STREAMFLAGS \_ xxx

Especifica as características que um cliente pode atribuir a um fluxo de áudio durante a inicialização do fluxo.



| Constante/valor                                                                                                                                                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | O fluxo de áudio será um membro de uma sessão de áudio de processo cruzado. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_ 0x00020000 de \_ auto-retorno STREAMFLAGS**</dt> <dt></dt> </dl>                                                   | O fluxo de áudio funcionará no modo de loopback. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK**</dt> <dt>0x00040000</dt> </dl>                                    | O processamento do buffer de áudio pelo cliente será controlado por eventos. Para obter mais informações, consulte Comentários. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ nopersist**</dt> <dt>0x00080000</dt> </dl>                                                | As configurações de volume e mudo para uma sessão de áudio não serão mantidas entre as reinicializações do aplicativo. Para obter mais informações, consulte Comentários.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | Essa constante é nova no Windows 7. A taxa de amostragem do fluxo é ajustada para uma taxa especificada por um aplicativo. Para obter mais informações, consulte Comentários. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**</dt> <dt>0x80000000</dt> </dl>                                 | Um matriz de canal e um conversor de taxa de amostra são inseridos conforme necessário para converter entre o formato descompactado fornecido para [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) e o formato de combinação de mecanismo de áudio.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ src \_ padrão de \_ qualidade**</dt> <dt>0x08000000</dt> </dl>                | Quando usado com **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**, um conversor de taxa de amostra com melhor qualidade do que a conversão padrão, mas com um custo de desempenho mais alto é usado. Isso deve ser usado se o áudio for basicamente destinado a ser ouvido por seres humanos em oposição a outros cenários, como a bombeamento de silêncio ou o preenchimento de um medidor.<br/> |



## <a name="remarks"></a>Comentários

O método [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) e a estrutura de parâmetros de ativação de áudio do DirectX usam as constantes AUDCLNT [**\_ \_ \_**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) \_ STREAMFLAGS \_ xxx.

O \_ sinalizador AUDCLNT STREAMFLAGS \_ CROSSPROCESS indica que a sessão de áudio para o fluxo é uma sessão de processo cruzado. Uma sessão entre processos pode aceitar fluxos de mais de um processo. Se dois aplicativos em dois processos separados chamarem **IAudioClient:: Initialize** com GUIDs de sessão idênticos e os dois aplicativos definirem o \_ sinalizador CROSSPROCESS AUDCLNT ShareMode \_ , o mecanismo de áudio atribuirá seus fluxos à mesma sessão entre processos. Esse sinalizador substitui o comportamento padrão, que é atribuir o fluxo a uma sessão específica do processo em vez de uma sessão entre processos. O \_ bit de sinalizador AUDCLNT STREAMFLAGS \_ CROSSPROCESS é incompatível com o modo exclusivo. Para obter mais informações sobre sessões de processo cruzado, consulte [sessões de áudio](audio-sessions.md).

O \_ sinalizador de auto-retorno AUDCLNT STREAMFLAGS habilita a gravação de \_ loopback. Na gravação de auto-retorno, o mecanismo de áudio copia o fluxo de áudio que está sendo reproduzido por um dispositivo de ponto de extremidade de renderização em um buffer de ponto de extremidade de áudio para que um cliente [WASAPI](wasapi.md) possa capturar o fluxo. Se esse sinalizador for definido, o método **IAudioClient:: Initialize** tentará abrir um buffer de captura no dispositivo de renderização. Esse sinalizador só é válido para um dispositivo de renderização e somente se a chamada de **inicialização** definir o parâmetro *ShareMode* como \_ compartilhado AUDCLNT ShareMode \_ . Caso contrário, a chamada de **inicialização** falhará. Se a chamada for realizada com sucesso, o cliente poderá chamar o método [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) para obter uma interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) no dispositivo de renderização. Para obter mais informações, consulte [gravação de auto-retorno](loopback-recording.md).

O \_ sinalizador AUDCLNT STREAMFLAGS \_ EVENTCALLBACK habilita o buffer controlado por eventos. Se um cliente definir esse sinalizador na chamada para **IAudioClient:: Initialize** que inicializa um fluxo, o cliente deverá chamar subseqüentemente o método [**IAudioClient:: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) para fornecer um identificador de evento para o fluxo. Depois que o fluxo é iniciado, o mecanismo de áudio sinalizará o identificador de evento para notificar o cliente sempre que um buffer ficar pronto para o cliente processar. O WASAPI dá suporte ao buffer controlado por evento para os buffers de renderização e de captura. O modo compartilhado e os fluxos de modo exclusivo podem usar o buffer controlado por eventos. Para obter um exemplo de código que usa \_ o \_ sinalizador AUDCLNT STREAMFLAGS EVENTCALLBACK, consulte [fluxos de modo exclusivo](exclusive-mode-streams.md).

O \_ sinalizador AUDCLNT STREAMFLAGS \_ nopersist desabilita a persistência do volume e as configurações de mudo para uma sessão que contém fluxos de renderização. Por padrão, o nível de volume e o estado de mudo para uma sessão de renderização são persistentes entre as reinicializações do aplicativo. O nível de volume e o estado de mudo para uma sessão de captura nunca são persistentes. Para obter mais informações sobre a persistência do volume da sessão e as configurações de mudo, consulte [sessões de áudio](audio-sessions.md).

O \_ sinalizador AUDCLNT STREAMFLAGS \_ RATEADJUST permite que um aplicativo obtenha uma referência à interface [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) que é usada para definir a taxa de amostragem para o fluxo. Para obter um ponteiro para esse interface, um aplicativo deve inicializar o cliente de áudio com esse sinalizador e, em seguida, chamar [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) especificando o identificador **\_ IAudioClockAdjustment do IID** . Para definir a nova taxa de amostra, chame [**IAudioClockAdjustment:: Setamostrate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate). Esse sinalizador é válido somente para um dispositivo de renderização. Caso contrário, a chamada **GetService** falhará com o código de erro AUDCLNT \_ E \_ tipo de ponto de extremidade incorreto \_ \_ . O aplicativo também deve definir o parâmetro *ShareMode* como AUDCLNT \_ ShareMode \_ compartilhado durante a chamada de [**inicialização**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . **Setsampleize** falha se o cliente de áudio não estiver no modo compartilhado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Principais constantes de áudio](core-audio-constants.md)
</dt> <dt>

[**Interface IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




