---
title: MCI_STATUS comando (mmsystem. h)
description: O \_ comando status do MCI recupera informações sobre um dispositivo MCI. Todos os dispositivos reconhecem este comando. As informações são retornadas no membro dwReturn da estrutura identificada pelo parâmetro lpStatus.
ms.assetid: d1c3dff9-c66f-4525-aac1-4a15b43083e7
keywords:
- Multimídia do Windows de comando MCI_STATUS
topic_type:
- apiref
api_name:
- MCI_STATUS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86553ac759a362c1ea4abb53a47d0e9376cbc526
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "104297787"
---
# <a name="mci_status-command"></a>Comando de status do MCI \_

> [!NOTE]
> Comunicação sem tendência a Microsoft dá suporte a um ambiente diversificado e de inclusão.  Neste documento, há referências à palavra ' escravo '. O [Guia de estilo da Microsoft para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) reconhece isso como uma palavra de exclusão.  Essa palavra-chave é usada, pois é atualmente a palavra usada nos comandos. Para fins de consistência, este documento contém esta palavra. Quando esta palavra for alterada nos comandos, corrigiremos este documento para estar em alinhamento.

O \_ comando status do MCI recupera informações sobre um dispositivo MCI. Todos os dispositivos reconhecem este comando. As informações são retornadas no membro **dwReturn** da estrutura identificada pelo parâmetro *lpStatus* .

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STATUS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_STATUS_PARMS) lpStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI. Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStatus"></span><span id="lpstatus"></span><span id="LPSTATUS"></span>*lpStatus*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros de status MCI**](mci-status-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores padrão adicionais e específicos de comando se aplicam a todos os dispositivos que dão suporte ao status do MCI \_ :

<dl> <dt>

<span id="MCI_STATUS_ITEM"></span><span id="mci_status_item"></span>\_item de status MCI \_
</dt> <dd>

Especifica que o membro **dwItem** da estrutura identificada por *lpStatus* contém uma constante especificando qual item de status obter. As constantes a seguir definem qual item de status deve ser retornado no membro **dwReturn** da estrutura:

\_ \_ rastreamento atual do status do MCI \_

O membro **dwReturn** é definido como o número de faixa atual. O MCI usa números de faixa contínuos.

\_comprimento do status MCI \_

O membro **dwReturn** é definido como o comprimento total da mídia.

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modo de status MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o modo atual do dispositivo. Os modos incluem o seguinte:

-   \_modo MCI \_ não \_ está pronto
-   \_pausa no modo MCI \_
-   \_reprodução do modo MCI \_
-   \_parada do modo MCI \_
-   \_modo MCI \_ aberto
-   \_registro do modo MCI \_
-   \_modo MCI \_ Seek

</dd> <dt>

<span id="MCI_STATUS_NUMBER_OF_TRACKS"></span><span id="mci_status_number_of_tracks"></span>\_status \_ do MCI número \_ de \_ faixas
</dt> <dd>

O membro **dwReturn** é definido como o número total de faixas reproduzidas.

</dd> <dt>

<span id="MCI_STATUS_POSITION"></span><span id="mci_status_position"></span>\_posição do status do MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a posição atual.

</dd> <dt>

<span id="MCI_STATUS_READY"></span><span id="mci_status_ready"></span>STATUS do MCI \_ \_ pronto
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo estiver pronto; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_STATUS_TIME_FORMAT"></span><span id="mci_status_time_format"></span>\_formato de \_ tempo de status do MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o formato de hora atual do dispositivo. Os formatos de hora incluem:

-   \_bytes de formato MCI \_
-   \_quadros de formato MCI \_
-   \_formato MCI \_ HMS
-   \_milissegundos do formato MCI \_
-   \_formato MCI \_ MSF
-   \_exemplos de formato MCI \_
-   \_formato MCI \_ TMSF

</dd> <dt>

<span id="MCI_STATUS_START"></span><span id="mci_status_start"></span>\_início do status do MCI \_
</dt> <dd>

Obtém a posição inicial da mídia. Para obter a posição inicial, combine esse sinalizador com \_ o item de status MCI \_ e defina o membro **dwItem** da estrutura identificada por *lpStatus* para a posição do \_ status MCI \_ .

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>\_faixa MCI
</dt> <dd>

Indica que um parâmetro de faixa de status está incluído no membro **dwTrack** da estrutura identificada por *lpStatus*. Você deve usar esse sinalizador com a posição do status do MCI ou com as \_ \_ constantes de comprimento do status do MCI \_ \_ . Quando usado com a \_ \_ posição do status MCI, \_ a faixa MCI Obtém a posição inicial da faixa especificada. Quando usado com o \_ \_ comprimento do status MCI, \_ a faixa MCI Obtém o comprimento da faixa especificada. O MCI usa números de faixa contínuos.

</dd> </dl>

Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **cdaudio** . Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .

<dl> <dt>

<span id="MCI_CDA_STATUS_TYPE_TRACK"></span><span id="mci_cda_status_type_track"></span>\_faixa de \_ tipo de status \_ \_ do MCI CDA
</dt> <dd>

O membro **dwReturn** é definido como um dos seguintes valores:

-   áudio de controle do MCI \_ CDA \_ \_
-   \_ \_ outro controle do MCI CDA \_

Para usar esse sinalizador, o \_ sinalizador de faixa MCI deve ser definido e o membro **dwTrack** da estrutura identificada por *lpStatus* deve conter um número de faixa válido.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente
</dt> <dd>

O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_STATUS_DISKSPACE"></span><span id="mci_dgv_status_diskspace"></span>espaço em disco de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **lpstrDrive** da estrutura identificada por *lpStatus* especifica uma unidade de disco ou, em algumas implementações, um caminho. O \_ comando status do MCI retorna a quantidade aproximada de espaço em disco que pode ser obtida pelo comando de [ \_ reserva do MCI](mci-reserve.md) no membro **dwReturn** da estrutura identificada por *lpStatus*. O espaço em disco é medido em unidades do formato de hora atual.

</dd> <dt>

<span id="MCI_DGV_STATUS_INPUT"></span><span id="mci_dgv_status_input"></span>\_entrada de \_ status MCI DGV \_
</dt> <dd>

A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* se aplica à entrada.

</dd> <dt>

<span id="MCI_DGV_STATUS_LEFT"></span><span id="mci_dgv_status_left"></span>\_status do DGV MCI \_ \_ restante
</dt> <dd>

A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* se aplica ao canal de áudio à esquerda.

</dd> <dt>

<span id="MCI_DGV_STATUS_NOMINAL"></span><span id="mci_dgv_status_nominal"></span>STATUS de DGV do MCI \_ \_ \_ nominal
</dt> <dd>

A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* solicita o valor nominal em vez do valor atual.

</dd> <dt>

<span id="MCI_DGV_STATUS_OUTPUT"></span><span id="mci_dgv_status_output"></span>\_saída de \_ status de DGV MCI \_
</dt> <dd>

A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* se aplica à saída.

</dd> <dt>

<span id="MCI_DGV_STATUS_RECORD"></span><span id="mci_dgv_status_record"></span>\_registro de \_ status do DGV MCI \_
</dt> <dd>

A taxa de quadros retornada para o \_ sinalizador de taxa de quadros do status do MCI DGV \_ \_ \_ é a taxa usada para compactação.

</dd> <dt>

<span id="MCI_DGV_STATUS_REFERENCE"></span><span id="mci_dgv_status_reference"></span>referência de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** da estrutura identificada por *lpStatus* retorna a imagem de quadro chave mais próxima que precede o quadro especificado no membro **dwReference** .

</dd> <dt>

<span id="MCI_DGV_STATUS_RIGHT"></span><span id="mci_dgv_status_right"></span>\_status de DGV MCI \_ \_ direito
</dt> <dd>

A constante especificada pelo membro **dwItem** da estrutura identificada por *lpStatus* se aplica ao canal de áudio correto.

</dd> </dl>

As constantes a seguir são usadas com o tipo de dispositivo **DigitalVideo** no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .

<dl> <dt>

<span id="MCI_AVI_STATUS_AUDIO_BREAKS"></span><span id="mci_avi_status_audio_breaks"></span>\_ \_ \_ quebras de áudio de status \_ do MCI avi
</dt> <dd>

O membro **dwReturn** retorna o número de vezes que a parte de áudio da última sequência AVI se quebrou. O sistema conta uma quebra de áudio sempre que tenta gravar dados de áudio no driver de dispositivo e descobre que o driver já reproduziu todos os dados disponíveis. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_FRAMES_SKIPPED"></span><span id="mci_avi_status_frames_skipped"></span>quadros de status do MCI \_ AVI \_ \_ \_ ignorados
</dt> <dd>

O membro **dwReturn** retorna o número de quadros que não foram desenhados quando a última sequência AVI foi reproduzida. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_STATUS_LAST_PLAY_SPEED"></span><span id="mci_avi_status_last_play_speed"></span>\_velocidade da \_ \_ última \_ reprodução \_ do status do MCI avi
</dt> <dd>

O membro **dwReturn** retorna um valor que representa a precisão da hora de execução real da última sequência AVI correspondente ao tempo de execução de destino. O valor 1000 indica que a hora de destino e a hora real foram as mesmas. Um valor de 2000, por exemplo, indicaria que a sequência AVI levou duas vezes mais tempo que deveria ter. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO"></span><span id="mci_dgv_status_audio"></span>áudio de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna \_ o MCI ou o MCI, \_ dependendo da opção de áudio de conjunto MCI mais recente \_ \_ para o comando [ \_ set do MCI](mci-set.md) . Ele retornará \_ o MCI em se um ou ambos os alto-falantes estiverem habilitados e o MCI não estiver em \_ contrário.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_INPUT"></span><span id="mci_dgv_status_audio_input"></span>\_entrada de \_ áudio de status MCI DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o nível de áudio instantâneo aproximado do sinal de áudio analógico. Um valor maior que 1000 implica que há distorção de recorte. Alguns dispositivos podem determinar esse valor somente durante a gravação de áudio. Esse valor de status não tem o comando **MCI \_ set** ou [MCI \_ SetAudio](mci-setaudio.md) associado. Esse valor está relacionado a, mas normalizado de forma diferente do, o nível de status de onda MCI do comando Wave-Audio \_ \_ \_ .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_RECORD"></span><span id="mci_dgv_status_audio_record"></span>\_registro de \_ áudio de status MCI DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna \_ o MCI ativado ou \_ o MCI, refletindo o estado definido pelo \_ \_ \_ sinalizador de gravação do DGV do MCI do comando do **MCI \_ SetAudio** .

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_SOURCE"></span><span id="mci_dgv_status_audio_source"></span>\_fonte de \_ áudio de status MCI DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna a fonte do digitalizador de áudio atual:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVERAGE"></span><span id="mci_dgv_setaudio_average"></span>\_média de DGV do MCI \_ \_
</dt> <dd>

Especifica a média dos canais de áudio esquerdo e direito.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ setáudio \_ esquerdo
</dt> <dd>

Especifica o canal de áudio à esquerda.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>\_DGV de \_ som \_ do MCI
</dt> <dd>

Especifica o canal de áudio correto.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STEREO"></span><span id="mci_dgv_setaudio_stereo"></span>\_estéreo de \_ áudio DGV \_ MCI
</dt> <dd>

Especifica o estéreo.

</dd> <dt>

<span id="MCI_DGV_STATUS_AUDIO_STREAM"></span><span id="mci_dgv_status_audio_stream"></span>\_fluxo de \_ áudio de status MCI DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o número de fluxo de áudio atual.

</dd> <dt>

<span id="MCI_DGV_STATUS_AVGBYTESPERSEC"></span><span id="mci_dgv_status_avgbytespersec"></span>AVGBYTESPERSEC de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o número médio de bytes por segundo usados para gravação.

</dd> <dt>

<span id="MCI_DGV_STATUS_BASS"></span><span id="mci_dgv_status_bass"></span>STATUS do MCI \_ DGV \_ \_ Bass
</dt> <dd>

O membro **dwReturn** retorna o nível de sons de áudio atual. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERPEL"></span><span id="mci_dgv_status_bitsperpel"></span>BITSPERPEL de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o número de bits por pixel usado para salvar dados capturados ou gravados.

</dd> <dt>

<span id="MCI_DGV_STATUS_BITSPERSAMPLE"></span><span id="mci_dgv_status_bitspersample"></span>BITSPERSAMPLE de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o número de bits por amostra que o dispositivo usa para gravação. Isso se aplica somente a dispositivos que dão suporte ao formato PCM.

</dd> <dt>

<span id="MCI_DGV_STATUS_BLOCKALIGN"></span><span id="mci_dgv_status_blockalign"></span>BLOCKALIGN de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o alinhamento dos blocos de dados em relação ao início da onda de entrada.

</dd> <dt>

<span id="MCI_DGV_STATUS_BRIGHTNESS"></span><span id="mci_dgv_status_brightness"></span>brilho do status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o nível de brilho do vídeo atual. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_COLOR"></span><span id="mci_dgv_status_color"></span>cor de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o nível de cor atual. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_CONTRAST"></span><span id="mci_dgv_status_contrast"></span>\_contraste de \_ status do DGV MCI \_
</dt> <dd>

O membro **dwReturn** retorna o nível de contraste atual. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILEFORMAT"></span><span id="mci_dgv_status_fileformat"></span>\_formato de fileDGV de \_ status do MCI \_
</dt> <dd>

O membro **dwReturn** retorna o formato de arquivo atual para gravação ou salvamento.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_MODE"></span><span id="mci_dgv_status_file_mode"></span>\_modo de \_ arquivo de status DGV \_ MCI \_
</dt> <dd>

O membro **dwReturn** retorna o estado da operação de arquivo:

\_edição do \_ modo de arquivo MCI DGV \_ \_

Retornado durante operações de recortar, copiar, excluir, colar e desfazer.

\_modo de \_ arquivo DGV MCI \_ \_ ocioso

Retornado quando o arquivo está pronto para a próxima operação.

\_carregamento do \_ modo de arquivo DGV \_ MCI \_

Retornado enquanto o arquivo está sendo carregado.

\_salvamento do \_ modo de arquivo DGV \_ MCI \_

Retornado enquanto o arquivo está sendo salvo.

</dd> <dt>

<span id="MCI_DGV_STATUS_FILE_COMPLETION"></span><span id="mci_dgv_status_file_completion"></span>\_conclusão do \_ arquivo de status DGV \_ MCI \_
</dt> <dd>

O membro **dwReturn** retorna a porcentagem estimada em que uma operação de carregamento, gravação, captura, recorte, cópia, exclusão, colagem ou desfazer foi progredida. (Os aplicativos podem usar isso para fornecer um indicador visual de progresso.) Não há suporte para esse sinalizador em todos os dispositivos de vídeo digital.

</dd> <dt>

<span id="MCI_DGV_STATUS_FORWARD"></span><span id="mci_dgv_status_forward"></span>\_ \_ encaminhamento de status DGV MCI \_
</dt> <dd>

O membro **dwReturn** retornará **true** se a direção do dispositivo estiver encaminhada ou o dispositivo não estiver sendo reproduzido.

</dd> <dt>

<span id="MCI_DGV_STATUS_FRAME_RATE"></span><span id="mci_dgv_status_frame_rate"></span>\_taxa de \_ quadros de status \_ \_ do MCI DGV
</dt> <dd>

O membro **dwReturn** deve ser usado com o \_ status de DGV do MCI \_ \_ nominal, \_ \_ o registro de status do MCI DGV \_ ou ambos. Quando usado com o \_ registro de status MCI DGV \_ \_ , a taxa de quadros atual usada para gravação é retornada. Quando usado com \_ \_ o registro de status MCI DGV \_ e \_ status de DGV MCI \_ \_ nominal, a taxa de quadros nominal associada ao sinal de vídeo de entrada é retornada. Quando usado com \_ o status de DGV do MCI \_ \_ nominal, a taxa de quadros nominal associada ao arquivo é retornada. Em todos os casos, as unidades estão em quadros por segundo multiplicadas por 1000.

</dd> <dt>

<span id="MCI_DGV_STATUS_GAMMA"></span><span id="mci_dgv_status_gamma"></span>DGV do status do MCI \_ \_ \_ gama
</dt> <dd>

O membro **dwReturn** retorna o valor de gama atual. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_HPAL"></span><span id="mci_dgv_status_hpal"></span>HPAL de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o valor decimal ASCII para o identificador de paleta atual. O identificador está contido na palavra de ordem inferior do valor retornado.

</dd> <dt>

<span id="MCI_DGV_STATUS_HWND"></span><span id="mci_dgv_status_hwnd"></span>\_HWND de \_ status \_ DGV do MCI
</dt> <dd>

O membro **dwReturn** retorna o valor decimal ASCII para o identificador de janela explícito ou padrão atual associado a esta instância de driver de dispositivo. O identificador está contido na palavra de ordem inferior do valor retornado.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_COLOR"></span><span id="mci_dgv_status_key_color"></span>\_cor da \_ chave de status \_ \_ do MCI DGV
</dt> <dd>

O membro **dwReturn** retorna o valor de cor de chave atual.

</dd> <dt>

<span id="MCI_DGV_STATUS_KEY_INDEX"></span><span id="mci_dgv_status_key_index"></span>\_índice de \_ chave de status MCI DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o valor de índice de chave atual.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR"></span><span id="mci_dgv_status_monitor"></span>\_Monitor de \_ status do DGV MCI \_
</dt> <dd>

O membro **dwReturn** retorna uma constante que indica a origem da apresentação atual. As seguintes constantes são definidas:

\_arquivo de \_ Monitor de DGV MCI \_

Um arquivo é a origem.

\_entrada do \_ Monitor de DGV MCI \_

A entrada é a origem.

</dd> <dt>

<span id="MCI_DGV_STATUS_MONITOR_METHOD"></span><span id="mci_dgv_status_monitor_method"></span>\_método de \_ Monitor de status DGV \_ MCI \_
</dt> <dd>

O membro **dwReturn** retorna uma constante indicando o método usado para o monitoramento de entrada. As seguintes constantes são definidas:

\_método MCI \_ DGV \_ direto

Monitoramento de entrada direto.

\_post do \_ método MCI DGV \_

Monitoramento de pós-entrada.

\_método MCI \_ DGV \_ pre

Monitoramento de pré-entrada.

</dd> <dt>

<span id="MCI_DGV_STATUS_PAUSE_MODE"></span><span id="mci_dgv_status_pause_mode"></span>\_modo de \_ pausa de status \_ \_ do MCI DGV
</dt> <dd>

O membro **dwReturn** retorna o \_ modo MCI \_ Play se o dispositivo foi pausado durante a reprodução e \_ retorna \_ o registro do modo MCI se o dispositivo foi pausado durante a gravação. O comando retornará MCIERR \_ \_ função não aplicável como um erro retornado se o dispositivo não estiver em pausa.

</dd> <dt>

<span id="MCI_DGV_STATUS_SAMPLESPERSECOND"></span><span id="mci_dgv_status_samplespersecond"></span>SAMPLESPERSECOND de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna o número de amostras por segundo registradas.

</dd> <dt>

<span id="MCI_DGV_STATUS_SEEK_EXACTLY"></span><span id="mci_dgv_status_seek_exactly"></span>STATUS do MCI \_ DGV \_ \_ Seek \_ exactly
</dt> <dd>

O membro **dwReturn** retorna **true** ou **false** indicando se o formato de busca exata está definido ou não. (Os aplicativos podem definir esse formato usando o comando [MCI \_ set](mci-set.md) com o \_ sinalizador MCI DGV \_ set \_ Seek \_ Exact.)

</dd> <dt>

<span id="MCI_DGV_STATUS_SHARPNESS"></span><span id="mci_dgv_status_sharpness"></span>\_nitidez do \_ status do DGV MCI \_
</dt> <dd>

O membro **dwReturn** retorna o nível de nitidez atual. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_SIZE"></span><span id="mci_dgv_status_size"></span>\_tamanho do \_ status do DGV MCI \_
</dt> <dd>

O membro **dwReturn** retorna a duração de reprodução aproximada dos dados compactados que o espaço de trabalho reservado irá manter. As unidades de duração estão no formato de hora atual. Ele retornará zero se não houver espaço reservado em disco. O tamanho retornado é aproximado, pois o espaço em disco preciso para dados compactados não pode, em geral, ser previsto até que os dados tenham sido compactados.

</dd> <dt>

<span id="MCI_DGV_STATUS_SMPTE"></span><span id="mci_dgv_status_smpte"></span>STATUS do MCI \_ DGV \_ \_ SMPTE
</dt> <dd>

O membro **dwReturn** retorna o código de tempo SMPTE associado à posição atual no espaço de trabalho.

</dd> <dt>

<span id="MCI_DGV_STATUS_SPEED"></span><span id="mci_dgv_status_speed"></span>\_velocidade de \_ status do DGV MCI \_
</dt> <dd>

O membro **dwReturn** retorna a velocidade de reprodução atual.

</dd> <dt>

<span id="MCI_DGV_STATUS_STILL_FILEFORMAT"></span><span id="mci_dgv_status_still_fileformat"></span>o \_ status do MCI DGV \_ ainda é \_ \_ FileFormat
</dt> <dd>

O membro **dwReturn** retorna o formato de arquivo atual para o comando de [ \_ captura MCI](mci-capture.md) .

</dd> <dt>

<span id="MCI_DGV_STATUS_TINT"></span><span id="mci_dgv_status_tint"></span>\_tonalidade de \_ status MCI DGV \_
</dt> <dd>

O membro **dwReturn** retorna o nível de tonalidade de vídeo atual. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_TREBLE"></span><span id="mci_dgv_status_treble"></span>STATUS do MCI \_ DGV \_ \_ agudo
</dt> <dd>

O membro **dwReturn** retorna o nível de agudos de áudio atual. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_UNSAVED"></span><span id="mci_dgv_status_unsaved"></span>\_status de DGV MCI \_ \_ não salvo
</dt> <dd>

O membro **dwReturn** retornará **true** se houver dados gravados no espaço de trabalho que podem ser perdidos como resultado de um [ \_ fechamento MCI](mci-close.md), [ \_ carregamento de MCI](mci-load.md), [ \_ registro MCI](mci-record.md), [ \_ reserva de MCI](mci-reserve.md), [ \_ recorte de MCI](mci-cut.md), [ \_ exclusão](mci-delete.md)de MCI ou comando de [ \_ colar MCI](mci-paste.md) . Caso contrário, o membro retornará **false** .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO"></span><span id="mci_dgv_status_video"></span>vídeo de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retornará o MCI se o \_ vídeo estiver habilitado ou o MCI \_ desativado se estiver desabilitado.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_RECORD"></span><span id="mci_dgv_status_video_record"></span>\_registro de \_ vídeo de status \_ \_ do MCI DGV
</dt> <dd>

O membro **dwReturn** retorna \_ o MCI ativado ou o MCI \_ desativado, refletindo o estado definido \_ pelo \_ \_ sinalizador de gravação do DGV do MCI do comando do [MCI \_](mci-setvideo.md) .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SOURCE"></span><span id="mci_dgv_status_video_source"></span>\_fonte de \_ vídeo de status MCI DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna uma constante que indica o tipo de fonte de vídeo definido pelo \_ sinalizador de origem do DGV \_ do MCI \_ do comando do **MCI \_ setvideo** .

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_SRC_NUM"></span><span id="mci_dgv_status_video_src_num"></span>\_número de \_ \_ src de vídeo de status DGV \_ MCI \_
</dt> <dd>

O membro **dwReturn** retorna o número dentro do seu tipo da fonte de entrada de vídeo ativa no momento.

</dd> <dt>

<span id="MCI_DGV_STATUS_VIDEO_STREAM"></span><span id="mci_dgv_status_video_stream"></span>\_fluxo de \_ vídeo de status \_ \_ do MCI DGV
</dt> <dd>

O membro **dwReturn** retorna o número de fluxo de vídeo atual.

</dd> <dt>

<span id="MCI_DGV_STATUS_VOLUME"></span><span id="mci_dgv_status_volume"></span>VOLUME de status do MCI \_ DGV \_ \_
</dt> <dd>

O membro **dwReturn** retorna a média do volume para os alto-falantes esquerdo e direito. Use \_ \_ o status do DGV MCI \_ nominal com esse sinalizador para obter o nível nominal.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_VISIBLE"></span><span id="mci_dgv_status_window_visible"></span>janela de status do MCI \_ DGV \_ \_ \_ visível
</dt> <dd>

O membro **dwReturn** retornará **true** se a janela não estiver oculta.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MINIMIZED"></span><span id="mci_dgv_status_window_minimized"></span>janela de status do MCI \_ DGV \_ \_ \_ minimizada
</dt> <dd>

O membro **dwReturn** retornará **true** se a janela for minimizada.

</dd> <dt>

<span id="MCI_DGV_STATUS_WINDOW_MAXIMIZED"></span><span id="mci_dgv_status_window_maximized"></span>janela de status do MCI \_ DGV \_ \_ \_ maximizada
</dt> <dd>

O membro **dwReturn** retornará **true** se a janela for maximizada.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente
</dt> <dd>

O membro **dwReturn** retorna **true**.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpStatus* aponta para uma estrutura de [**\_ \_ \_ parâmetros de status DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_status_parmsa) .

Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **Sequencer** . Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .

<dl> <dt>

<span id="MCI_SEQ_STATUS_DIVTYPE"></span><span id="mci_seq_status_divtype"></span>\_DIVTYPE de \_ status de Seq MCI \_
</dt> <dd>

O membro **dwReturn** é definido como um dos seguintes valores indicando o tipo de divisão atual de uma sequência:

-   MCI \_ Seq \_ div \_ PPQN
-   MCI \_ Seq \_ div \_ SMPTE \_ 24
-   MCI \_ Seq \_ div \_ SMPTE \_ 25
-   MCI \_ Seq \_ div \_ SMPTE \_ 30
-   MCI \_ Seq \_ div \_ SMPTE \_ 30DROP

</dd> <dt>

<span id="MCI_SEQ_STATUS_MASTER"></span><span id="mci_seq_status_master"></span>\_mestre de \_ status de Seq MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o tipo de sincronização usado para a operação mestre.

</dd> <dt>

<span id="MCI_SEQ_STATUS_OFFSET"></span><span id="mci_seq_status_offset"></span>\_deslocamento de \_ status de Seq MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o deslocamento SMPTE atual de uma sequência.

</dd> <dt>

<span id="MCI_SEQ_STATUS_PORT"></span><span id="mci_seq_status_port"></span>porta de status do MCI \_ Seq \_ \_
</dt> <dd>

O membro **dwReturn** é definido como o identificador do dispositivo MIDI para a porta atual usada pela sequência.

</dd> <dt>

<span id="MCI_SEQ_STATUS_SLAVE"></span><span id="mci_seq_status_slave"></span>\_auxiliar Seq de \_ status \_ do MCI
</dt> <dd>

O membro **dwReturn** é definido como o tipo de sincronização usado para a operação subordinada.

</dd> <dt>

<span id="MCI_SEQ_STATUS_TEMPO"></span><span id="mci_seq_status_tempo"></span>\_tempo de \_ status de Seq MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o tempo atual de uma sequência MIDI em batidas por minuto para arquivos PPQN ou quadros por segundo para arquivos SMPTE.

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente
</dt> <dd>

O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .

</dd> </dl>

Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **VCR** . Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente
</dt> <dd>

O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_ASSEMBLE_RECORD"></span><span id="mci_vcr_status_assemble_record"></span>\_registro de \_ montagem do status do VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** será definido como **true** se o modo de montagem estiver on; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR"></span><span id="mci_vcr_status_audio_monitor"></span>\_Monitor de \_ áudio de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante, indicando o tipo de monitor de áudio selecionado no momento.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_MONITOR_NUMBER"></span><span id="mci_vcr_status_audio_monitor_number"></span>\_número do \_ \_ Monitor de \_ áudio \_ MCI de status do VCR
</dt> <dd>

O membro **dwReturn** é definido como o número do tipo de monitor de áudio selecionado no momento.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_RECORD"></span><span id="mci_vcr_status_audio_record"></span>\_registro de \_ áudio de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** será definido como **true** se o áudio for gravado quando o próximo comando de registro for fornecido; caso contrário, será definido como **false** . Se você especificar a \_ faixa MCI no parâmetro *dwFlags* deste comando, **dwTrack** conterá a faixa à qual essa consulta se aplica.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE"></span><span id="mci_vcr_status_audio_source"></span>\_fonte de \_ áudio de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante, indicando o tipo de fonte de áudio atual.

</dd> <dt>

<span id="MCI_VCR_STATUS_AUDIO_SOURCE_NUMBER"></span><span id="mci_vcr_status_audio_source_number"></span>\_número de \_ \_ fonte de \_ áudio \_ MCI de status do VCR
</dt> <dd>

O membro **dwReturn** é definido como o número do tipo de fonte de áudio selecionado no momento.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK"></span><span id="mci_vcr_status_clock"></span>\_relógio de \_ status do VCR MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o valor do relógio atual, em incrementos de clock totais.

</dd> <dt>

<span id="MCI_VCR_STATUS_CLOCK_ID"></span><span id="mci_vcr_status_clock_id"></span>\_ID do \_ relógio de status do VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como um número que descreve exclusivamente o relógio em uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_FORMAT"></span><span id="mci_vcr_status_counter_format"></span>\_formato do \_ contador de status do VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante que descreve o formato do contador atual. Para obter mais informações, consulte o \_ \_ \_ sinalizador de formato de tempo do MCI set do comando do [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_COUNTER_RESOLUTION"></span><span id="mci_vcr_status_counter_resolution"></span>\_resolução do \_ contador de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante que descreve a resolução do contador e é um dos seguintes valores:

-   \_ \_ \_ \_ Quadros de resolução do contador de VCR MCI: o contador tem resolução de quadros.
-   \_ \_ \_ Segundos de res do contador de videocassete MCI: o \_ contador tem a resolução de segundos.
-   \_Valor do \_ contador de status do VCR MCI \_ \_ : o membro **dwReturn** é definido como a leitura do contador atual, no formato de tempo do contador atual.

</dd> <dt>

<span id="MCI_VCR_STATUS_FRAME_RATE"></span><span id="mci_vcr_status_frame_rate"></span>\_taxa de \_ quadros de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como a taxa de quadros nativa atual do dispositivo.

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX"></span><span id="mci_vcr_status_index"></span>\_índice de \_ status de VCR MCI \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante, descrevendo o conteúdo atual da exibição na tela e é um dos seguintes:

-   \_contador de \_ índice de VCR MCI \_
-   \_data do \_ índice de VCR do MCI \_
-   \_tempo de \_ índice de VCR do MCI \_
-   código de meio do \_ índice de VCR MCI \_ \_

</dd> <dt>

<span id="MCI_VCR_STATUS_INDEX_ON"></span><span id="mci_vcr_status_index_on"></span>\_ \_ \_ índice de status de VCR MCI \_ em
</dt> <dd>

O membro **dwReturn** será definido como **true** se a exibição na tela estiver on; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_MEDIA_TYPE"></span><span id="mci_vcr_status_media_type"></span>\_tipo de \_ mídia de status do VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como um dos seguintes:

-   Mídia de VCR MCI com \_ \_ \_ 8mm
-   \_Mídia VCR \_ MCI \_ Hi8
-   \_VHS de \_ mídia \_ VCR MCI
-   \_mídia VCR \_ MCI \_ SVHS
-   mídia de VCR do MCI \_ \_ \_ beta
-   \_mídia VCR \_ MCI \_ EDBETA
-   \_mídia de VCR MCI \_ \_ diferente

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER"></span><span id="mci_vcr_status_number"></span>\_número de \_ status do VCR MCI \_
</dt> <dd>

O membro **dwNumber** é definido como o número do sintonizador lógico quando você usa esse sinalizador com o \_ sinalizador de canal do \_ sintonizador de status do VCR MCI \_ \_ .

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_AUDIO_TRACKS"></span><span id="mci_vcr_status_number_of_audio_tracks"></span>\_ \_ status do VCR \_ MCI \_ número \_ de \_ faixas de áudio
</dt> <dd>

O membro **dwReturn** é definido como o número de faixas de áudio que são selecionáveis de forma independente.

</dd> <dt>

<span id="MCI_VCR_STATUS_NUMBER_OF_VIDEO_TRACKS"></span><span id="mci_vcr_status_number_of_video_tracks"></span>\_ \_ status do VCR \_ MCI \_ número \_ de \_ faixas de vídeo
</dt> <dd>

O membro **dwReturn** é definido como o número de faixas de vídeo que são selecionáveis de forma independente.

</dd> <dt>

<span id="MCI_VCR_STATUS_PAUSE_TIMEOUT"></span><span id="mci_vcr_status_pause_timeout"></span>\_ \_ \_ tempo limite de pausa de status de VCR MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a duração máxima, em milissegundos, de um comando PAUSE. O valor de retorno de zero indica que nenhum tempo limite ocorrerá.

</dd> <dt>

<span id="MCI_VCR_STATUS_PLAY_FORMAT"></span><span id="mci_vcr_status_play_format"></span>\_formato de \_ reprodução de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como um dos seguintes:

-   \_EP de \_ formato \_ VCR MCI
-   \_formato de videocassete MCI \_ \_ LP
-   \_ \_ outro formato de VCR MCI \_
-   \_SP de \_ formato \_ VCR MCI

</dd> <dt>

<span id="MCI_VCR_STATUS_POSTROLL_DURATION"></span><span id="mci_vcr_status_postroll_duration"></span>\_duração de \_ redistribuição de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como o tamanho da fita de vídeo que será reproduzida após o ponto em que foi interrompido, no formato de hora atual. Isso é necessário para desposicionar o transporte de fita do VCR de um comando parar ou pausar.

</dd> <dt>

<span id="MCI_VCR_STATUS_POWER_ON"></span><span id="mci_vcr_status_power_on"></span>\_ \_ \_ ativação de status de VCR MCI \_ em
</dt> <dd>

O membro **dwReturn** será definido como **true** se a energia estiver ativada; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_PREROLL_DURATION"></span><span id="mci_vcr_status_preroll_duration"></span>\_duração da \_ preversão do status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como o tamanho da fita de vídeo que será reproduzida antes do ponto em que ele foi iniciado, no formato de hora atual. Isso é necessário para estabilizar a saída do VCR.

</dd> <dt>

<span id="MCI_VCR_STATUS_RECORD_FORMAT"></span><span id="mci_vcr_status_record_format"></span>\_formato de \_ registro de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como um dos seguintes:

-   \_EP de \_ formato \_ VCR MCI
-   \_formato de videocassete MCI \_ \_ LP
-   \_ \_ outro formato de VCR MCI \_
-   \_SP de \_ formato \_ VCR MCI

</dd> <dt>

<span id="MCI_VCR_STATUS_SPEED"></span><span id="mci_vcr_status_speed"></span>\_velocidade de \_ status do VCR MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a velocidade atual. Para obter mais informações, consulte o \_ \_ \_ sinalizador de velocidade do conjunto de VCR MCI do comando [ \_ set do MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_MODE"></span><span id="mci_vcr_status_time_mode"></span>\_modo de \_ tempo de status do VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como um dos seguintes:

-   \_contador de \_ tempo de VCR MCI \_
-   \_detecção de \_ tempo de VCR MCI \_
-   tempo de vida de \_ hora do VCR MCI \_ \_

Para obter mais informações, consulte o \_ \_ \_ \_ sinalizador de modo de tempo de conjunto de VCR MCI do comando [ \_ set do MCI](mci-set.md) .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIME_TYPE"></span><span id="mci_vcr_status_time_type"></span>\_tipo de \_ tempo de status do VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante que descreve o tipo de hora atual em uso (usado por [Play](play.md), [Record](record.md), [Seek](seek.md)e assim por diante) e é um dos seguintes:

</dd> <dt>

<span id="MCI_VCR_TIME_COUNTER"></span><span id="mci_vcr_time_counter"></span>\_contador de \_ tempo de VCR MCI \_
</dt> <dd>

O contador está em uso.

</dd> <dt>

<span id="MCI_VCR_TIME_TIMECODE"></span><span id="mci_vcr_time_timecode"></span>tempo de vida de \_ hora do VCR MCI \_ \_
</dt> <dd>

O código de pafica em uso.

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_PRESENT"></span><span id="mci_vcr_status_timecode_present"></span>\_código de status de VCR MCI \_ \_ \_ presente
</dt> <dd>

O membro **dwReturn** será definido como **true** se o código de tempo estiver presente na posição atual no conteúdo; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_RECORD"></span><span id="mci_vcr_status_timecode_record"></span>\_registro de \_ código de status do VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** será definido como **true** se o código de code for registrado quando o próximo comando de registro for atribuído; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_VCR_STATUS_TIMECODE_TYPE"></span><span id="mci_vcr_status_timecode_type"></span>\_tipo de \_ código de status de VCR do MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante, descrevendo o tipo de código de erro que é diretamente suportado pelo dispositivo e é um dos seguintes:

-   \_Tipo de código de paficação de videocassete MCI \_ \_ \_ None: este dispositivo não usa um código de um.
-   \_ \_ Tipo de código de erro de VCR MCI \_ \_ outro: este dispositivo usa um código de erro não especificado.
-   \_Tipo de \_ código de pausar VCR MCI \_ \_ : este dispositivo usa o código de pausando SMPTE.
-   Tipo de código de caso de \_ VCR MCI \_ \_ \_ \_ drop ignore: este dispositivo usa o código de recurso de descarte SMPTE.

</dd> <dt>

<span id="MCI_VCR_STATUS_TUNER_CHANNEL"></span><span id="mci_vcr_status_tuner_channel"></span>\_canal de \_ \_ sintonização de status de VCR MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o número do canal atual. Se você especificar \_ \_ \_ o número de status do VCR MCI no parâmetro *dwFlags* deste comando, **dwNumber** conterá o número do sintonizador lógico ao qual esse comando se aplica.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR"></span><span id="mci_vcr_status_video_monitor"></span>\_Monitor de \_ vídeo de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante, indicando o tipo de monitor de vídeo selecionado no momento.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_MONITOR_NUMBER"></span><span id="mci_vcr_status_video_monitor_number"></span>\_número do \_ Monitor de vídeo do status do VCR MCI \_ \_ \_
</dt> <dd>

O membro **dwReturn** é definido como o número do tipo de monitor de vídeo selecionado no momento.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_RECORD"></span><span id="mci_vcr_status_video_record"></span>\_registro de \_ vídeo de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** será definido como **true** se o vídeo for gravado quando o próximo comando de registro for fornecido; caso contrário, será definido como **false** . Se você especificar a \_ faixa MCI no parâmetro *dwFlags* deste comando, **dwTrack** conterá a faixa à qual essa consulta se aplica.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE"></span><span id="mci_vcr_status_video_source"></span>\_fonte de \_ vídeo de status de VCR MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como uma constante que indica o tipo de fonte de vídeo selecionado no momento.

</dd> <dt>

<span id="MCI_VCR_STATUS_VIDEO_SOURCE_NUMBER"></span><span id="mci_vcr_status_video_source_number"></span>\_número de \_ fonte do vídeo de status do VCR MCI \_ \_ \_
</dt> <dd>

O membro **dwReturn** é definido como o número do tipo de fonte de vídeo selecionado no momento.

</dd> <dt>

<span id="MCI_VCR_STATUS_WRITE_PROTECTED"></span><span id="mci_vcr_status_write_protected"></span>\_status do VCR MCI \_ \_ \_ protegido contra gravação
</dt> <dd>

O membro **dwReturn** será definido como **true** se a mídia estiver protegida contra gravação; caso contrário, será definido como **false** .

</dd> </dl>

Para dispositivos VCR, o parâmetro *lpStatus* aponta para uma estrutura de parâmetros de [**status de \_ VCR \_ \_ MCI**](mci-vcr-status-parms.md) .

Usar o \_ sinalizador de \_ comprimento do status MCI para determinar o comprimento da mídia sempre retorna 2 horas para dispositivos VCR, a menos que o comprimento tenha sido explicitamente alterado usando o comando [MCI \_ set](mci-set.md) .

Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo de **sobreposição** . Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .

<dl> <dt>

<span id="MCI_OVLY_STATUS_HWND"></span><span id="mci_ovly_status_hwnd"></span>\_HWND de \_ status \_ OVLY do MCI
</dt> <dd>

O membro **dwReturn** é definido como o identificador da janela associada ao dispositivo de sobreposição de vídeo.

</dd> <dt>

<span id="MCI_OVLY_STATUS_STRETCH"></span><span id="mci_ovly_status_stretch"></span>\_Stretch de \_ status de OVLY MCI \_
</dt> <dd>

O membro **dwReturn** será definido como **true** se o alargamento estiver habilitado; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente
</dt> <dd>

O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .

</dd> </dl>

Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **VIDEODISC** . Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .

<dl> <dt>

<span id="MCI_STATUS_MEDIA_PRESENT"></span><span id="mci_status_media_present"></span>\_mídia de status MCI \_ \_ presente
</dt> <dd>

O membro **dwReturn** será definido como **true** se a mídia for inserida no dispositivo; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_STATUS_MODE"></span><span id="mci_status_mode"></span>\_modo de status MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o modo atual do dispositivo. Os dispositivos VIDEODISC podem retornar a \_ constante de estacionamento do modo de VD do MCI \_ \_ , além das constantes que qualquer dispositivo pode retornar, conforme documentado com o parâmetro *dwFlags* .

</dd> <dt>

<span id="MCI_VD_STATUS_DISC_SIZE"></span><span id="mci_vd_status_disc_size"></span>\_tamanho do \_ disco de status de VD do MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como o tamanho do disco carregado em polegadas (8 ou 12).

</dd> <dt>

<span id="MCI_VD_STATUS_FORWARD"></span><span id="mci_vd_status_forward"></span>\_avanço do \_ status de VD do MCI \_
</dt> <dd>

O membro **dwReturn** é definido como **true** se estiver tocando; caso contrário, será definido como **false** .

O dispositivo MCI VIDEODISC não dá suporte a esse sinalizador.

</dd> <dt>

<span id="MCI_VD_STATUS_MEDIA_TYPE"></span><span id="mci_vd_status_media_type"></span>\_tipo de \_ mídia de status de VD do MCI \_ \_
</dt> <dd>

O membro **dwReturn** é definido como o tipo de mídia da mídia inserida. Os seguintes tipos de mídia podem ser retornados:

\_cav de \_ mídia de VD do MCI \_

\_CLV de \_ mídia de VD do MCI \_

mídia de VD do MCI \_ \_ \_ diferente

</dd> <dt>

<span id="MCI_VD_STATUS_SIDE"></span><span id="mci_vd_status_side"></span>\_ \_ lado do status de VD \_ do MCI
</dt> <dd>

O membro **dwReturn** é definido como 1 ou 2 para indicar qual lado do disco está carregado. Nem todos os dispositivos VIDEODISC dão suporte a esse sinalizador.

</dd> <dt>

<span id="MCI_VD_STATUS_SPEED"></span><span id="mci_vd_status_speed"></span>\_velocidade de \_ status de VD do MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a velocidade de reprodução em quadros por segundo. O MCIPIONR. O driver de dispositivo DRV retorna MCIERR \_ função sem suporte \_ .

</dd> </dl>

Os sinalizadores adicionais a seguir são usados com o tipo de dispositivo **WaveAudio** . Essas constantes são usadas no membro **dwItem** da estrutura apontada pelo parâmetro *lpStatus* quando o \_ item de status MCI \_ é especificado para o parâmetro *dwFlags* .

<dl> <dt>

<span id="MCI_WAVE_FORMATTAG"></span><span id="mci_wave_formattag"></span>\_FORMATTAG Wave \_ MCI
</dt> <dd>

O membro **dwReturn** é definido como a marca de formato atual usada para reproduzir, gravar e salvar.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o dispositivo de entrada de onda usado para gravação. Se nenhum dispositivo estiver em uso e nenhum dispositivo tiver sido explicitamente definido, o retorno de erro será MCIERR \_ Wave \_ INPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_saída de onda MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o dispositivo de saída de onda usado para reprodução. Se nenhum dispositivo estiver em uso e nenhum dispositivo tiver sido explicitamente definido, o retorno de erro será MCIERR \_ Wave \_ OUTPUTUNSPECIFIED.

</dd> <dt>

<span id="MCI_WAVE_STATUS_AVGBYTESPERSEC"></span><span id="mci_wave_status_avgbytespersec"></span>\_AVGBYTESPERSEC de \_ status de onda MCI \_
</dt> <dd>

O membro **dwReturn** é definido para os bytes atuais por segundo usados para reprodução, gravação e salvamento.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BITSPERSAMPLE"></span><span id="mci_wave_status_bitspersample"></span>\_BITSPERSAMPLE de \_ status de onda MCI \_
</dt> <dd>

O membro **dwReturn** é definido para os bits atuais por amostra usados para reproduzir, gravar e salvar dados formatados PCM.

</dd> <dt>

<span id="MCI_WAVE_STATUS_BLOCKALIGN"></span><span id="mci_wave_status_blockalign"></span>\_BLOCKALIGN de \_ status de onda MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o alinhamento de bloco atual usado para reproduzir, gravar e salvar.

</dd> <dt>

<span id="MCI_WAVE_STATUS_CHANNELS"></span><span id="mci_wave_status_channels"></span>\_canais de \_ status de onda MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a contagem de canais atual usada para reproduzir, gravar e salvar.

</dd> <dt>

<span id="MCI_WAVE_STATUS_LEVEL"></span><span id="mci_wave_status_level"></span>\_nível de \_ status de onda MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o registro atual ou o nível de reprodução dos dados formatados do PCM. O valor é retornado como um valor de 8 ou 16 bits, dependendo do tamanho de amostra usado. O nível de canal direito ou mono é retornado na palavra de ordem inferior. O nível de canal esquerdo é retornado na palavra de ordem superior.

</dd> <dt>

<span id="MCI_WAVE_STATUS_SAMPLESPERSEC"></span><span id="mci_wave_status_samplespersec"></span>\_SAMPLESPERSEC de \_ status de onda MCI \_
</dt> <dd>

O membro **dwReturn** é definido para os exemplos atuais por segundo usados para reproduzir, gravar e salvar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> <dt>

[recorte de MCI \_](mci-cut.md)
</dt> <dt>

[exclusão de MCI \_](mci-delete.md)
</dt> <dt>

[\_colar MCI](mci-paste.md)
</dt> <dt>

[Reserva de MCI \_](mci-reserve.md)
</dt> <dt>

[conjunto de MCI \_](mci-set.md)
</dt> <dt>

[reproduzir](play.md)
</dt> <dt>

[gravável](record.md)
</dt> <dt>

[Procure](seek.md)
</dt> </dl>

 

