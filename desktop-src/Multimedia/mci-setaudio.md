---
title: MCI_SETAUDIO comando (mmsystem. h)
description: O \_ comando autoaudio do MCI define os valores associados à reprodução e à captura de áudio. Os dispositivos de vídeo digital e VCR reconhecem este comando.
ms.assetid: 78624596-e465-4ef1-8988-edcfe9a46f89
keywords:
- MCI_SETAUDIO comando Windows multimídia
topic_type:
- apiref
api_name:
- MCI_SETAUDIO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b882209b8a9debc2c01e4f5c6f852d418c1a5cd321a764af022d19c58fe32a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803393"
---
# <a name="mci_setaudio-command"></a>\_Comando de SETaudio do MCI

O \_ comando autoaudio do MCI define os valores associados à reprodução e à captura de áudio. Os dispositivos de vídeo digital e VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETAUDIO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetAudio
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

\_Notificação MCI, \_ espera MCI ou teste MCI \_ . Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSetAudio"></span><span id="lpsetaudio"></span><span id="LPSETAUDIO"></span>*lpSetAudio*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores se aplicam ao tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_SETAUDIO_ALG"></span><span id="mci_dgv_setaudio_alg"></span>ALG DGV do MCI de \_ \_ áudio \_
</dt> <dd>

O membro **lpstrAlgorithm** da estrutura identificada por *lpSetAudio* contém um endereço de um buffer que contém o nome de um algoritmo de compactação de áudio. O algoritmo de compactação é usado por comandos de [ \_ gravação MCI](mci-record.md) ou de [ \_ reserva de MCI](mci-reserve.md) subsequentes. Os algoritmos disponíveis são dependentes do dispositivo. Se o algoritmo for incompatível com o formato de arquivo atual, o formato de arquivo será alterado para o formato padrão do algoritmo.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_CLOCKTIME"></span><span id="mci_dgv_setaudio_clocktime"></span>\_DGV de \_ horário de áudio \_ do MCI
</dt> <dd>

O tempo especificado é em milissegundos e é o tempo absoluto quando usado com o MCI \_ DGV \_ \_ por áudio. (Esse tempo não está em etapa com a reprodução do espaço de trabalho.)

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_INPUT"></span><span id="mci_dgv_setaudio_input"></span>\_entrada de \_ SetAudio do MCI DGV \_
</dt> <dd>

Modifica o sinalizador Bass, agudos ou volume para que ele afete o sinal de entrada e modifique o que é registrado. Se possível, esse é o padrão ao monitorar a entrada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_ITEM"></span><span id="mci_dgv_setaudio_item"></span>\_item de \_ áudio DGV \_ MCI
</dt> <dd>

Uma constante de áudio é especificada no membro **dwItem** da estrutura identificada por *lpSetAudio*. A constante identifica o valor que está sendo definido. As seguintes constantes são definidas:

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_AVGBYTESPERSEC"></span><span id="mci_dgv_setaudio_avgbytespersec"></span>\_AVGBYTESPERSEC DGV \_ do MCI \_
</dt> <dd>

O número médio de bytes é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*. Esse valor define o número médio de bytes por segundo para reprodução ou gravação nos formatos PCM (modulação de código de pulso) e ADPCM (modulação diferencial de código de pulso). O arquivo é salvo neste formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BASS"></span><span id="mci_dgv_setaudio_bass"></span>MCI \_ DGV \_ SetAudio \_ Bass
</dt> <dd>

O nível de baixa frequência de áudio é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BITSPERSAMPLE"></span><span id="mci_dgv_setaudio_bitspersample"></span>\_BITSPERSAMPLE DGV \_ do MCI \_
</dt> <dd>

O número de bits por amostra é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*. Esse valor define o número de bits por amostra reproduzido ou registrado no formato PCM. O arquivo é salvo neste formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_BLOCKALIGN"></span><span id="mci_dgv_setaudio_blockalign"></span>\_BLOCKALIGN DGV \_ do MCI \_
</dt> <dd>

O alinhamento do bloco de dados é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*. Esse valor define o alinhamento dos blocos de dados em relação ao início dos dados de onda de entrada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SAMPLESPERSEC"></span><span id="mci_dgv_setaudio_samplespersec"></span>\_SAMPLESPERSEC DGV \_ do MCI \_
</dt> <dd>

A taxa de amostra é especificada no membro **dwValue** da estrutura identificada por *lpSetAudio*. Esse valor define a taxa de amostragem para reproduzir e gravar com os algoritmos PCM e ADPCM. O arquivo é salvo neste formato.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_SOURCE"></span><span id="mci_dgv_setaudio_source"></span>\_fonte de \_ áudio DGV do MCI \_
</dt> <dd>

Uma constante que especifica a fonte de entrada de áudio é incluída no membro **dwValue** da estrutura identificada por *lpSetAudio*. As constantes a seguir são definidas para as fontes de entrada de áudio:

\_média de \_ origem do \_ DGV do MCI \_

A média dos canais de áudio esquerdo e direito.

\_fonte de áudio DGV do MCI com a \_ \_ \_ esquerda

Canal de áudio à esquerda.

\_ \_ \_ origem \_ do DGV do MCI com fonte de áudio

Canal de áudio correto.

\_estéreo de \_ fonte de áudio MCI DGV \_ \_

Aparelhos.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_STREAM"></span><span id="mci_dgv_setaudio_stream"></span>\_fluxo de \_ áudio DGV \_ MCI
</dt> <dd>

Um fluxo de áudio é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*. O valor inteiro especifica o fluxo de áudio reproduzido do espaço de trabalho. Se o fluxo não for especificado, o primeiro fluxo de áudio fisicamente intercalado será reproduzido.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_TREBLE"></span><span id="mci_dgv_setaudio_treble"></span>MCI \_ DGV \_ de som \_
</dt> <dd>

O nível de alta frequência de áudio é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetAudio*.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VOLUME"></span><span id="mci_dgv_setaudio_volume"></span>\_volume de \_ áudio MCI \_ DGV
</dt> <dd>

O nível de áudio para um ou ambos os canais de áudio é especificado como um fator no membro **dwValue** da estrutura identificada por *lpSetAudio*. Se os volumes esquerdo e direito tiverem sido definidos com valores diferentes, a taxa do volume da esquerda para a direita será quase inalterada.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_LEFT"></span><span id="mci_dgv_setaudio_left"></span>MCI \_ DGV \_ setáudio \_ esquerdo
</dt> <dd>

Habilita o canal de áudio à esquerda quando usado com o MCI \_ definido \_ como ativado. Desabilita o canal de áudio à esquerda quando usado com o MCI \_ definido como \_ desativado. Quando esse sinalizador é usado com a combinação do valor de DGV do MCI \_ \_ e do \_ \_ \_ volume de áudio MCI DGV \_ , ele define o volume do canal de áudio à esquerda. Quando esse sinalizador é usado com a \_ \_ fonte de áudio MCI DGV \_ , ele especifica o canal de áudio à esquerda como a origem do digitalizador de entrada de áudio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_OVER"></span><span id="mci_dgv_setaudio_over"></span>MCI \_ DGV \_ por áudio \_
</dt> <dd>

Um parâmetro de comprimento de transição está incluído no membro **dwOver** da estrutura identificada por *lpSetAudio*. O valor de comprimento especifica quanto tempo (em unidades do formato de hora atual) deve ser necessário para fazer uma alteração que usa um fator. Se esse sinalizador não for usado, as alterações ocorrerão imediatamente.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_QUALITY"></span><span id="mci_dgv_setaudio_quality"></span>\_qualidade de \_ áudio DGV \_ MCI
</dt> <dd>

O membro **lpstrQuality** da estrutura identificada por *lpSetAudio* contém um endereço de um buffer que define a qualidade de áudio. Uma cadeia de caracteres de texto dentro do buffer especifica as características do algoritmo de compactação de áudio.

O \_ sinalizador de \_ alg DGV de autoáudio do MCI \_ pode ser usado para selecionar um descritor de qualidade para o algoritmo especificado. Se esse sinalizador for omitido, o algoritmo atual será usado.

Os algoritmos e os nomes de descritores disponíveis dependem do dispositivo. Cada dispositivo fornece documentação para os algoritmos disponíveis e uma descrição dos nomes de descritores aplicáveis. O comando de [ \_ qualidade do MCI](mci-quality.md) pode definir nomes de descritores adicionais.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RECORD"></span><span id="mci_dgv_setaudio_record"></span>\_registro de \_ áudio DGV \_ MCI
</dt> <dd>

Especifica se a gravação inclui ou exclui dados de áudio. Quando combinado com o MCI \_ definido \_ ativado, os dados de áudio são registrados. Quando combinado com o MCI \_ definido \_ , os dados de áudio são excluídos. O padrão inclui dados de áudio.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_RIGHT"></span><span id="mci_dgv_setaudio_right"></span>\_DGV de \_ som \_ do MCI
</dt> <dd>

Habilita o canal de áudio correto quando usado com o MCI \_ definido \_ como ativado. Desabilita o canal de áudio correto quando usado com o MCI \_ definido como \_ desativado. Quando esse sinalizador é usado com a combinação do valor de DGV do MCI \_ \_ e do \_ \_ \_ volume de áudio MCI DGV \_ , ele define o volume do canal de áudio correto.

</dd> <dt>

<span id="MCI_DGV_SETAUDIO_VALUE"></span><span id="mci_dgv_setaudio_value"></span>\_valor DGV \_ do MCI \_
</dt> <dd>

Um valor é especificado no membro **dwValue** da estrutura identificada por *lpSetAudio*. O significado do valor é especificado pela constante definida para o \_ sinalizador de item de áudio DGV do MCI \_ \_ .

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado
</dt> <dd>

Desabilita o canal de áudio especificado.

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em
</dt> <dd>

Habilita o canal de áudio especificado.

</dd> <dt>

<span id="MCI_SETAUDIO_OUTPUT"></span><span id="mci_setaudio_output"></span>\_saída de SETaudio do MCI \_
</dt> <dd>

Modifica o sinalizador Bass, agudos ou volume para que ele modifique apenas o sinal de reprodução e não o que é registrado. Se possível, esse é o padrão ao monitorar a entrada.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpSetAudio* aponta para uma estrutura de parâmetros de [**áudio do \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setaudio_parmsa) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_SETAUDIO_RECORD"></span><span id="mci_vcr_setaudio_record"></span>\_registro de \_ áudio de VCR MCI \_
</dt> <dd>

Define a gravação de áudio como on ou off, que é usada em conjunto com um dos seguintes sinalizadores:

MCI \_ definido \_ em

Gravação de áudio ativada.

conjunto de MCI \_ \_ desativado

Gravação de áudio desativada. Pode ser necessário primeiro desativar a gravação de montagem (usando o comando [MCI \_ set](mci-set.md) com o \_ conjunto de VCR MCI \_ definir \_ \_ sinalizador de registro de montagem definido como desativado) antes que a gravação de áudio possa ser desativada.

\_faixa MCI

O membro **dwTrack** da estrutura identificada por *lpSetAudio* especifica qual faixa é afetada pelo comando.

\_fonte de \_ áudio do VCR MCI \_

Define a fonte de áudio. Esse sinalizador deve ser usado com o sinalizador de áudio MCI do \_ VCR \_ \_ para sinalizar.

\_Monitor de \_ áudio de VCR MCI \_

Define o monitor de fonte de áudio. Esse sinalizador deve ser usado com o sinalizador de áudio MCI do \_ VCR \_ \_ para sinalizar.

\_vídeo de VCR do MCI \_ \_ para

O membro **dwTo** da estrutura identificada por *lpSetAudio* contém uma constante que descreve o tipo de entrada ou entrada monitorada. Ele deve ser um dos seguintes:

<dl> <dd>

\_ \_ \_ sintonizador de tipo de src VCR do MCI \_

O tipo é sintonizador.

</dd> <dd>

\_linha de \_ tipo de src VCR \_ MCI \_

O tipo é linha.

</dd> <dd>

\_tipo de \_ src do VCR \_ do MCI \_

O tipo é auxiliar.

</dd> <dd>

\_tipo de src VCR do MCI \_ \_ \_ genérico

O tipo é genérico.

</dd> <dd>

\_tipo de src de vídeo MCI \_ \_ \_ sem áudio

O tipo está mudo. Isso pode ser usado somente com o \_ sinalizador de fonte de vídeo do VCR MCI \_ \_ .

</dd> <dd>

\_saída do \_ tipo de src VCR \_ MCI \_

O tipo é saída.

</dd> <dd>

\_número de \_ áudio do VCR MCI \_

O membro dwNumber da estrutura identificada por lpSetAudio contém a entrada de áudio (do tipo especificado no membro dwTo) a ser usado.

</dd> </dl> </dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> <dt>


</dt> <dd></dd> </dl>

Para dispositivos VCR, o parâmetro *lpSetAudio* aponta para uma estrutura de parâmetros de [**áudio do \_ VCR \_ \_ MCI**](mci-vcr-setaudio-parms.md) .

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

 

