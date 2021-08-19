---
title: MCI_GETDEVCAPS comando (Mmsystem.h)
description: O comando \_ MCI GETDEVCAPS recupera informações estáticas sobre um dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS comando Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7798f72405209f9834c3b67f84e57508c58ffc6153bce860b91f089005648905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803947"
---
# <a name="mci_getdevcaps-command"></a>Comando \_ MCI GETDEVCAPS

O comando \_ MCI GETDEVCAPS recupera informações estáticas sobre um dispositivo. Todos os dispositivos reconhecem esse comando. Os parâmetros e sinalizadores disponíveis para esse comando dependem do dispositivo selecionado. As informações são retornadas no **membro dwReturn** da estrutura identificada por *lpCapsParms*.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI WAIT ou, para dispositivos de vídeo digital e \_ VCR, MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

Ponteiro para uma [**estrutura \_ MCI GETDEVCAPS \_ PARMS.**](mci-getdevcaps-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores padrão e específicos de comando adicionais se aplicam a todos os dispositivos que suportam MCI \_ GETDEVCAPS:

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>DISPOSITIVO \_ COMPOSTO MCI GETDEVCAPS \_ \_
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo usar o armazenamento de dados que deve ser aberto e fechado explicitamente; caso contrário, ele será **definido como FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>TIPO DE DISPOSITIVO \_ MCI GETDEVCAPS \_ \_
</dt> <dd>

O **membro dwReturn** é definido como um dos valores listados em Tipos de [Dispositivo MCI.](mci-device-types.md)

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ GETDEVCAPS \_ TEM \_ ÁUDIO
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo tiver saída de áudio; caso contrário, ele será **definido como FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ TEM \_ VÍDEO
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo tiver saída de vídeo; caso contrário, ele será **definido como FALSE.** Por exemplo, o membro é definido como **TRUE para dispositivos** que são compatíveis com o conjunto de comandos videodisc.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI \_ GETDEVCAPS \_ ITEM
</dt> <dd>

Especifica que o **membro dwItem** da estrutura [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) contém uma das seguintes constantes:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI \_ GETDEVCAPS \_ PODE \_ EJETAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder ejetar a mídia; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI \_ GETDEVCAPS \_ PODE \_ REPRODUZIR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder reproduzir a mídia; caso contrário, ele será definido como **FALSE.** Se um dispositivo especificar **TRUE**, isso implica que o dispositivo dá suporte aos comandos [MCI \_ PAUSE](mci-pause.md) e [MCI \_ STOP,](mci-stop.md) bem como ao [comando MCI \_ PLAY.](mci-play.md)

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ GETDEVCAPS \_ PODE \_ REGISTRAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo for compatível com a gravação; caso contrário, ele será definido como **FALSE.** Se um dispositivo especificar **TRUE**, isso implica que o dispositivo dá suporte aos comandos MCI PAUSE e MCI STOP, bem como \_ ao comando \_ [MCI \_ RECORD.](mci-record.md)

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI \_ GETDEVCAPS \_ PODE \_ SALVAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE** se o dispositivo puder salvar um arquivo; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ GETDEVCAPS \_ USA \_ ARQUIVOS
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo exigir um nome de arquivo; caso contrário, ele será **definido como FALSE.** Somente dispositivos compostos usam arquivos.

</dd> </dl>

Os seguintes sinalizadores podem ser especificados no membro **dwItem** do [**\_ MCI GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para o tipo de dispositivo **digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ DGV \_ GETDEVCAPS \_ PODE \_ CONGELAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder congelar quadros; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI \_ DGV \_ GETDEVCAPS \_ PODE \_ BLOQUEAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder bloquear; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI \_ DGV \_ GETDEVCAPS \_ PODE \_ REVERTER
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder reproduzir em ordem inversa; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ PODE \_ STR \_ EM
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder ampliar a entrada; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI \_ DGV \_ GETDEVCAPS \_ PODE SE \_ ALONGAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder ampliar uma imagem; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI \_ DGV \_ GETDEVCAPS \_ PODE \_ TESTAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder executar testes; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ AINDA \_ TEM
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder exibir imagens ainda; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

O **membro dwReturn** é definido como o número máximo de janelas que o dispositivo pode manipular simultaneamente.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>TAXA MÁXIMA \_ DE \_ GETDEVCAPS DE DGV \_ DA \_ MCI
</dt> <dd>

O **membro dwReturn** é definido como a taxa de reprodução máxima para o dispositivo, em quadros por segundo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI \_ DGV \_ GETDEVCAPS \_ TAXA \_ MÍNIMA
</dt> <dd>

O **membro dwReturn** é definido como a taxa de reprodução mínima para o dispositivo, em quadros por segundo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>PALETAS \_ \_ GETDEVCAPS MCI DGV \_
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder retornar um alça de paleta; caso contrário, ele será definido como **FALSE.**

</dd> </dl>

Os seguintes sinalizadores podem ser especificados no **membro dwItem** do [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para o **tipo de dispositivo vcr:**

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>TAXA DE INCREMENTO DO RELÓGIO \_ MCI GETDEVCAPS \_ \_ \_
</dt> <dd>

O **membro dwReturn** é definido como o número de incrementos por segundo.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>O \_ VCR \_ GETDEVCAPS DA MCI \_ PODE DETECTAR O \_ \_ COMPRIMENTO
</dt> <dd>

O **membro dwReturn** será definido como **TRUE** se o dispositivo for capaz de detectar o comprimento da mídia; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>O \_ VCR \_ GETDEVCAPS DA MCI \_ PODE \_ CONGELAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo for capaz de congelar a imagem de saída; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>O \_ VCR \_ GETDEVCAPS DA MCI \_ PODE MONITORAR \_ \_ FONTES
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo for capaz de monitorar fontes; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>O \_ VCR GETDEVCAPS DA MCI \_ PODE FAZER O \_ \_ PRÉ-ROLL
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo for capaz de fazer o pré-roll; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>O \_ VCR \_ GETDEVCAPS DA MCI \_ PODE SER \_ VISUALIZADO
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo for capaz de visualizações; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>O \_ VCR \_ GETDEVCAPS DA MCI \_ PODE \_ REVERTER
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo for capaz de tocar em ordem inversa; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>O MCI \_ VCR \_ GETDEVCAPS \_ PODE \_ TESTAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo for capaz de testar; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI \_ VCR \_ GETDEVCAPS \_ TEM \_ RELÓGIO
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo for compatível com um relógio externo; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>O \_ VCR \_ GETDEVCAPS DA MCI \_ TEM O CÓDIGO DE \_ HORA
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo tiver a funcionalidade de código de data/hora ou se essa funcionalidade for desconhecida; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>NÚMERO DE MARCAS \_ \_ GETDEVCAPS DO VCR \_ \_ DA MCI \_
</dt> <dd>

O **membro dwReturn** é definido como o número de marcas (99).

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>PRECISÃO DA BUSCA \_ \_ DE GETDEVCAPS DO VCR \_ DA \_ MCI
</dt> <dd>

O **membro dwReturn** é definido como a precisão de busca do dispositivo.

</dd> </dl>

Os seguintes sinalizadores podem ser especificados no membro **dwItem** do [**\_ MCI GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para o tipo **de** dispositivo de sobreposição:

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>O MCI \_ OVLY \_ GETDEVCAPS \_ PODE \_ CONGELAR
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder congelar a imagem; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>O MCI \_ OVLY \_ GETDEVCAPS \_ PODE SER \_ ESTENDIDO
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o dispositivo puder ampliar a imagem para preencher o quadro; caso contrário, ele será definido como **FALSE.**

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ MAX \_ WINDOWS
</dt> <dd>

O **membro dwReturn** é definido como o número máximo de janelas que o dispositivo pode manipular simultaneamente.

</dd> </dl>

Os seguintes sinalizadores podem ser especificados no **membro dwItem** do [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para o tipo de dispositivo **videodisc:**

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI \_ VD \_ GETDEVCAPS \_ PODE \_ REVERTER
</dt> <dd>

O **membro dwReturn** será definido como **TRUE se** o player videodisc puder reproduzir ao contrário; caso contrário, ele será definido como **FALSE.** Alguns jogadores podem reproduzir discos CLV em ordem inversa, bem como discos DE VALOR.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ GETDEVCAPSLC \_
</dt> <dd>

Quando combinado com outros itens, especifica que as informações de retorno se aplica a videodiscs de formato DECOD. Esse será o padrão se nenhum videodisc for inserido.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ GETDEVCAPS \_ CLV
</dt> <dd>

Quando combinado com outros itens, especifica que as informações de retorno se aplica a videodiscs de formato CLV.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI \_ VD \_ GETDEVCAPS \_ FAST \_ TAXA
</dt> <dd>

O **membro dwReturn** é definido como a taxa de reprodução rápida padrão em quadros por segundo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>TAXA \_ NORMAL DE \_ GETDEVCAPS \_ DA MCI VD \_
</dt> <dd>

O **membro dwReturn** é definido como a taxa de reprodução normal em quadros por segundo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>TAXA LENTA \_ DE \_ GETDEVCAPS \_ DA MCI VD \_
</dt> <dd>

O **membro dwReturn** é definido como a taxa de reprodução lenta padrão em quadros por segundo.

</dd> </dl>

Os seguintes sinalizadores podem ser especificados no **membro dwItem** do [**MCI \_ GETDEVCAPS \_ PARMS**](mci-getdevcaps-parms.md) para o tipo de dispositivo **waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>ENTRADA \_ \_ GETDEVCAPS DA MCI WAVE \_
</dt> <dd>

O **membro dwReturn** é definido como o número total de dispositivos de entrada de forma de onda (gravação).

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>SAÍDA \_ \_ GETDEVCAPS DA MCI WAVE \_
</dt> <dd>

O **membro dwReturn** é definido como o número total de dispositivos de saída de forma de onda (reprodução).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

