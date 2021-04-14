---
title: MCI_SETVIDEO comando (mmsystem. h)
description: O \_ comando AddVideo do MCI define os valores associados à reprodução de vídeo. Os dispositivos de vídeo digital e VCR reconhecem este comando.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- Multimídia do Windows de comando MCI_SETVIDEO
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455201"
---
# <a name="mci_setvideo-command"></a>Comando do vídeo do MCI \_

O \_ comando AddVideo do MCI define os valores associados à reprodução de vídeo. Os dispositivos de vídeo digital e VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
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

**MCI \_ NOTIFICAÇÃO**, **\_ espera do MCI** ou **\_ teste MCI**. Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo "DigitalVideo":

<dl> <dt>

<span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>\_DGV de \_ vídeo do \_ MCI
</dt> <dd>

O membro **lpstrAlgorithm** da estrutura identificada por *lpSetVideo* contém um endereço de um buffer que contém o nome de um algoritmo de compactação de vídeo. O algoritmo de compactação é usado por comandos de [ \_ gravação MCI](mci-record.md) ou de [ \_ reserva de MCI](mci-reserve.md) subsequentes. Os algoritmos disponíveis são dependentes do dispositivo.

Se o algoritmo especificado for incompatível com o formato de arquivo atual, o formato de arquivo será alterado para o formato padrão do algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>\_DGV de \_ relógio de setvideo do MCI \_
</dt> <dd>

Quando usado com **o \_ DGV de \_ vídeo \_ MCI**, indica que o tempo é especificado em milissegundos e é o tempo absoluto. (Esse tempo não está em etapa com a reprodução do espaço de trabalho.)

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_entrada do DGV do MCI \_ \_
</dt> <dd>

Modifica o **\_ \_ \_ brilho do DGV MCI**, a **\_ \_ \_ cor do DGV do MCI**, o MCI DGV setvideo **\_ \_ \_ contraste**, **o \_ MCI DGV \_ setvideo \_ gama**, a **\_ \_ \_ nitidez do MCI DGV** ou a **\_ \_ \_ tonalidade de vídeo** do MCI DGV para que ele afete o sinal de entrada e modifique o que é registrado. Se possível, esse é o padrão ao monitorar a entrada.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_item de DGV do MCI \_ \_
</dt> <dd>

Uma constante de vídeo é especificada no membro **dwItem** da estrutura identificada por *lpSetVideo*. A constante identifica o valor que está sendo definido. Você pode especificar as seguintes constantes com este sinalizador:

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>\_procedimento de \_ desenho de vídeo do AVI do MCI \_ \_
</dt> <dd>

Um novo endereço de procedimento de desenho é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*. Você pode especificar um novo procedimento de desenho somente quando o dispositivo estiver ocioso. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI. Não há nenhum equivalente a esse sinalizador na interface de comando de cadeia de caracteres.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_cor da \_ paleta de vídeo do AVI do MCI \_ \_
</dt> <dd>

Uma nova cor de paleta é especificada nos membros **dwOver** e **dwValue** da estrutura identificada por *lpSetVideo*. O membro **dwOver** especifica o índice da paleta da cor a ser alterada e o membro **dwValue** especifica a nova cor, como um valor RGB. Você também deve especificar os sinalizadores de **\_ \_ \_ valor** do MCI **\_ DGV \_ \_** e do MCI DGV com o **\_ \_ \_ Item** de vídeo MCI DGV ao usar essa constante. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_meio- \_ Tom da \_ paleta de vídeo do AVI do MCI \_
</dt> <dd>

Indica que a paleta de meio-tom deve ser usada, em vez da paleta padrão. Esse sinalizador é reconhecido somente pelo driver de vídeo digital MCIAVI.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>\_BITSPERPEL DGV \_ do MCI \_
</dt> <dd>

O número de bits por pixel é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*. O número de bits por pixel é usado para salvar dados capturados ou gravados

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>\_brilho do DGV do MCI \_ \_
</dt> <dd>

O nível de brilho do vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_cor do DGV do MCI \_ \_
</dt> <dd>

O nível de saturação da cor do vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>\_contraste de DGV do MCI \_ \_
</dt> <dd>

O nível de contraste do vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_taxa de \_ quadros do \_ DGV do MCI \_
</dt> <dd>

Uma taxa de quadros é especificada no membro **dwValue** da estrutura identificada por *lpSetVideo*. A taxa é especificada em unidades de quadros por segundo, em vez de 1000. Por exemplo, 29,97 quadros por segundo é especificado como 29970.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>\_gama de DGV do MCI \_ \_
</dt> <dd>

Um valor de expoente de correção gama é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*. A correção gama ajusta o mapeamento entre a intensidade codificada na fonte da apresentação e o brilho exibido. O valor é o expoente multiplicado por 1000. Por exemplo, 2200 indica um expoente de 2,2. Um valor de 1000 indica um expoente de 1, que não se aplica a nenhuma correção de gama.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>\_cor da \_ chave do \_ DGV do MCI \_
</dt> <dd>

Uma cor de chave é especificada no membro **dwValue** da estrutura identificada por *lpSetVideo*. A cor da chave é um valor RGB.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_índice de \_ chave do \_ DGV do MCI \_
</dt> <dd>

Um valor de índice de chave é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*. O parâmetro de índice é um índice de paleta física.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>\_PALHANDLE DGV \_ do MCI \_
</dt> <dd>

Um identificador de paleta é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*. O identificador da paleta está contido na palavra de ordem inferior. Os dispositivos de vídeo digital não devem liberar a paleta passada com esse comando. Os aplicativos devem liberá-lo depois que fecharem o dispositivo. Esse sinalizador tem suporte apenas em dispositivos que usam paletas. Se esse identificador de paleta especificado for zero, a paleta padrão será usada.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_nitidez do DGV do MCI \_ \_
</dt> <dd>

Um valor de nitidez de vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>\_fonte de \_ vídeo MCI \_ DGV
</dt> <dd>

Uma constante especificando a origem da entrada de vídeo é especificada no membro **dwValue** da estrutura identificada por *lpSetVideo*. As seguintes constantes são definidas:

-   **MCI \_ DGV de \_ vídeo \_ src \_ NTSC**: televisão NTSC.
-   DGV de vídeo do MCI \_ PAL- \_ Video \_ src \_ : PAL televisão.
-   Vídeo do MCI \_ DGV do \_ vídeo \_ src \_ RGB: RGB.
-   DGV secam do MCI de \_ \_ vídeo \_ \_ : SECAM televisão.
-   \_DGV \_ de SVIDEO do MCI de vídeo \_ \_ : S-Video.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_fluxo de DGV do MCI \_ \_
</dt> <dd>

Um fluxo de vídeo é especificado no membro **dwValue** da estrutura identificada por *lpSetVideo*. O valor inteiro especifica o fluxo de vídeo reproduzido do espaço de trabalho. Se o fluxo não for especificado e o formato de arquivo não definir um fluxo padrão, o primeiro fluxo de vídeo intercalado fisicamente será reproduzido.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_tonalidade do DGV MCI \_ \_
</dt> <dd>

Um valor de tonalidade de vídeo é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetVideo*. Normalmente, esse ajuste é modelado após o controle de tonalidade de muitos conjuntos de televisão de cor, com 250 definido como verde, 750 definido como vermelho e 0 (ou 1000) definido como azul. O valor nominal é sempre 500.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_saída do DGV do MCI \_ \_
</dt> <dd>

O **\_ DGV de \_ \_ brilho do MCI**, **a \_ \_ \_ cor do vídeo MCI DGV**, o MCI DGV setvideo **\_ \_ \_ contraste**, o **MCI \_ DGV \_ setvideo \_ gama**, a **\_ \_ \_ nitidez do MCI DGV** ou o sinalizador de **\_ \_ \_ tonalidade do vídeo MCI DGV** é modificado para que ele afete apenas o sinal exibido e não o que é registrado. Se possível, esse é o padrão ao monitorar um arquivo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>\_DGV de \_ vídeo MCI \_
</dt> <dd>

Um parâmetro de comprimento de transição está incluído no membro **dwOver** da estrutura identificada por *lpSetVideo*. O comprimento da transição especifica quanto tempo (no formato de hora atual) deve ser necessário para fazer uma alteração. Se esse sinalizador não for usado, a alteração ocorrerá imediatamente.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>\_qualidade de \_ vídeo DGV \_ MCI
</dt> <dd>

O membro **lpstrQuality** da estrutura identificada por *lpSetVideo* contém um endereço de um buffer que descreve a qualidade do vídeo. Uma cadeia de texto no buffer especifica as características do algoritmo de compactação de vídeo.

O sinalizador de **\_ \_ \_ alg DGV do MCI de vídeo** pode ser usado para selecionar um descritor de qualidade para o algoritmo especificado. Se esse sinalizador for omitido, o algoritmo atual será usado.

Os algoritmos e os nomes de descritores disponíveis dependem do dispositivo. Cada dispositivo fornece documentação para os algoritmos disponíveis e uma descrição dos nomes de descritores aplicáveis. O comando de [ \_ qualidade do MCI](mci-quality.md) pode definir nomes de descritores adicionais. Todos os dispositivos dão suporte aos descritores "Low", "Medium" e "High". O padrão é específico do driver.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>\_registro do DGV do MCI \_ \_
</dt> <dd>

Especifica se a gravação inclui ou exclui dados de vídeo. Quando combinado com o **MCI \_ definido \_ como ativado**, os dados de vídeo são registrados. Quando combinado com **o \_ MCI \_ definido**, os dados de vídeo são excluídos. O padrão inclui dados de vídeo.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>\_ \_ \_ número src de DGV do \_ MCI
</dt> <dd>

Um número para a fonte de vídeo é especificado no membro **dwSourceNumber** da estrutura identificada por *lpSetVideo*. Se houver mais de uma entrada do tipo especificado pelo **\_ \_ \_ valor de DGV do MCI**, o valor selecionará a entrada. Esse sinalizador deve sempre ser usado com **a \_ \_ \_ fonte de vídeo MCI DGV**. Se **o \_ \_ \_ valor de DGV do MCI** for omitido, no entanto, o número de origem especificado indicará a origem absoluta a ser usada conforme especificado no comando da [ \_ lista de MCI](mci-list.md) .

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>o \_ DGV do MCI \_ \_
</dt> <dd>

O nome do algoritmo ou o valor de qualidade especificado se aplica às imagens do ainda.

Cada driver de dispositivo deve dar suporte a um algoritmo de "nenhum", o que significa que não há compactação. Esse é o padrão. Nesse caso, os dispositivos de vídeo digital salvam imagens ainda como bitmaps independentes de dispositivo (DIBs) RGB.

</dd> <dt>

<span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_valor do DGV do MCI \_ \_
</dt> <dd>

Um valor é incluído no membro **dwValue** da estrutura identificada por *lpSetVideo*. O significado do valor é especificado pelo sinalizador de **\_ \_ \_ item de vídeo DGV MCI** .

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado
</dt> <dd>

Desabilita a saída de vídeo. Para dispositivos de vídeo digital, desabilitar o vídeo define os pixels no retângulo de destino definido pelo comando [MCI \_ Put](mci-put.md) (ou seu padrão, a região cliente da janela atual) para uma cor sólida, mas não tem efeito sobre o buffer de quadro. Você pode ocultar a janela com o comando de [ \_ janela MCI](mci-window.md) , se desejado. A origem do vídeo, seja o espaço de trabalho ou uma entrada externa, pode continuar armazenando novas imagens no buffer de quadros, mas elas não são exibidas até que o vídeo seja habilitado. Embora os aplicativos devam usar o \_ comando AUTOVIDEO MCI para controlar essa função, os dispositivos de vídeo digital ainda devem dar suporte a esse sinalizador. O valor padrão após um Open é on.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em
</dt> <dd>

Habilita a saída de vídeo.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpSetVideo* aponta para uma estrutura de [**\_ \_ \_ parâmetros de vídeo DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo "VCR":

<dl> <dt>

<span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_registro de \_ vídeo de VCR MCI \_
</dt> <dd>

Define a gravação de vídeo como ativada ou desativada. Usado em conjunto com um dos seguintes sinalizadores:

-   **MCI \_ DEFINIDO \_ em**. Gravação de vídeo ativada.
-   **MCI \_ definido como \_ desativado**. Gravação de vídeo desativada. Pode ser necessário primeiro desativar a gravação de montagem (usando o comando [MCI \_ set](mci-set.md) com o conjunto de **VCR MCI Definir sinalizador de \_ \_ \_ \_ registro de montagem** definido como desativado) antes que a gravação de vídeo possa ser desativada.

</dd> <dt>

<span id="MCI_TRACK"></span><span id="mci_track"></span>\_faixa MCI
</dt> <dd>

O membro **dwTrack** da estrutura identificada por *lpSetVideo* especifica qual faixa é afetada pelo comando.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_fonte de \_ vídeo do VCR MCI \_
</dt> <dd>

Define a fonte de vídeo e deve ser usada com a marca de **\_ vídeo do VCR MCI \_ \_ para** sinalizar.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_Monitor de \_ vídeo de VCR MCI \_
</dt> <dd>

Define o monitor de fonte de vídeo e deve ser usado com o conjunto de \_ vídeos do VCR MCI \_ \_ para sinalizar.

</dd> <dt>

<span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>\_vídeo de VCR do MCI \_ \_ para
</dt> <dd>

O membro **dwTo** da estrutura identificada por *lpSetVideo* contém uma das seguintes constantes:

<dl> <dd>**\_ \_ \_ sintonizador de tipo de src VCR do MCI \_**</dd> <dd>**\_linha de \_ tipo de src VCR \_ MCI \_**</dd> <dd>**\_tipo de \_ src do VCR \_ do MCI \_**</dd> <dd>**\_tipo de src VCR do MCI \_ \_ \_ genérico**</dd> <dd>**\_tipo de src de vídeo MCI \_ \_ \_ sem áudio**</dd> <dd>**\_saída do \_ tipo de src VCR \_ MCI \_**</dd> <dd>**\_tipo de src VCR do MCI \_ \_ \_ RGB**</dd> <dd>**\_número de \_ vídeo do VCR MCI \_**</dd> </dl>

O membro **dwNumber** da estrutura identificada por *lpSetVideo* contém a entrada de vídeo (do tipo especificado no membro **dwTo** ) a ser usado.

</dd> </dl>

Para dispositivos VCR, o parâmetro *lpSetVideo* aponta para uma estrutura de parâmetros de [**vídeo do \_ VCR \_ \_ MCI**](mci-vcr-setvideo-parms.md) .

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
</dt> </dl>

 

