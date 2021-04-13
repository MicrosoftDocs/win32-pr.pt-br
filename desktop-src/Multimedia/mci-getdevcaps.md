---
title: MCI_GETDEVCAPS comando (mmsystem. h)
description: O \_ comando MCI GETDEVCAPS recupera informações estáticas sobre um dispositivo.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- Multimídia do Windows de comando MCI_GETDEVCAPS
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
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499796"
---
# <a name="mci_getdevcaps-command"></a>\_Comando MCI GETDEVCAPS

O \_ comando MCI GETDEVCAPS recupera informações estáticas sobre um dispositivo. Todos os dispositivos reconhecem este comando. Os parâmetros e sinalizadores disponíveis para este comando dependem do dispositivo selecionado. As informações são retornadas no membro **dwReturn** da estrutura identificada por *lpCapsParms*.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI. Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros MCI do GETDEVCAPS**](mci-getdevcaps-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores padrão adicionais e específicos de comando se aplicam a todos os dispositivos que dão suporte a \_ GETDEVCAPS MCI:

<dl> <dt>

<span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_dispositivo de \_ composição MCI GETDEVCAPS \_
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo usar o armazenamento de dados que deve ser aberto e fechado explicitamente; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_tipo de \_ dispositivo MCI GETDEVCAPS \_
</dt> <dd>

O membro **dwReturn** é definido como um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>o MCI \_ GETDEVCAPS \_ tem \_ áudio
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo tiver a saída de áudio; caso contrário, será definido como **false** .

</dd> <dt>

<span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ GETDEVCAPS \_ tem \_ vídeo
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo tiver saída de vídeo; caso contrário, será definido como **false** . Por exemplo, o membro é definido como **true** para dispositivos que dão suporte ao conjunto de comandos VIDEODISC.

</dd> <dt>

<span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_Item GETDEVCAPS \_ MCI
</dt> <dd>

Especifica que o membro **dwItem** da estrutura [**do \_ GETDEVCAPS \_ parms do MCI**](mci-getdevcaps-parms.md) contém uma das seguintes constantes:

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>o MCI \_ GETDEVCAPS \_ pode \_ ejetar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder ejetar a mídia; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>o MCI \_ GETDEVCAPS \_ pode \_ reproduzir
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder reproduzir a mídia; caso contrário, ele será definido como **false**. Se um dispositivo especificar **true**, ele implica que o dispositivo dá suporte aos comandos MCI [ \_ Pause](mci-pause.md) e [MCI \_ Stop](mci-stop.md) , bem como ao comando de [ \_ reprodução MCI](mci-play.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>o MCI \_ GETDEVCAPS \_ pode \_ gravar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo der suporte à gravação; caso contrário, ele será definido como **false**. Se um dispositivo especificar **true**, ele implica que o dispositivo dá suporte aos \_ comandos MCI Pause e MCI \_ Stop, bem como ao comando de [ \_ registro MCI](mci-record.md) .

</dd> <dt>

<span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>o MCI \_ GETDEVCAPS \_ pode \_ salvar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder salvar um arquivo; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>o MCI \_ GETDEVCAPS \_ usa \_ arquivos
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo exigir um nome de arquivo; caso contrário, será definido como **false** . Somente dispositivos compostos usam arquivos.

</dd> </dl>

Os sinalizadores a seguir podem ser especificados no membro **dwItem** do [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ congelar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder congelar quadros; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ Bloquear
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder ser bloqueado; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ reverter
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder reproduzir em ordem inversa; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI \_ DGV \_ GETDEVCAPS \_ pode \_ Str \_
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder ampliar a entrada; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ alongar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder alongar uma imagem; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>\_GETDEVCAPS MCI \_ DGV \_ pode \_ testar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder executar testes; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ DGV \_ GETDEVCAPS \_ \_ ainda
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder exibir imagens ainda; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI \_ DGV \_ GETDEVCAPS \_ Max \_ Windows
</dt> <dd>

O membro **dwReturn** é definido como o número máximo de janelas que o dispositivo pode manipular simultaneamente.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>\_ \_ taxa máxima de GETDEVCAPS DGV \_ MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a taxa máxima de reprodução para o dispositivo, em quadros por segundo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>\_ \_ taxa mínima de GETDEVCAPS DGV \_ MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a taxa de execução mínima para o dispositivo, em quadros por segundo.

</dd> <dt>

<span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ paletas MCI DGV GETDEVCAPS \_
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder retornar um identificador de paleta; caso contrário, ele será definido como **false**.

</dd> </dl>

Os sinalizadores a seguir podem ser especificados no membro **dwItem** dos [**\_ \_ parâmetros MCI GETDEVCAPS**](mci-getdevcaps-parms.md) para o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>\_taxa de \_ \_ incremento do relógio do GETDEVCAPS MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o número de incrementos por segundo.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ detectar \_ comprimento
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo for capaz de detectar o tamanho da mídia; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ congelar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo for capaz de congelar a imagem de saída; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ monitorar \_ fontes
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo for capaz de monitorar fontes; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode ser \_ prevertido
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder ser prevertido; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode ser \_ visualizado
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo for capaz de visualizações; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ reverter
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo for capaz de reproduzir em ordem inversa; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ pode \_ testar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo for capaz de testar; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>o \_ GETDEVCAPS do VCR MCI \_ \_ tem \_ relógio
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo der suporte a um relógio externo; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>o \_ GETDEVCAPS de videocassete do MCI \_ tem um \_ \_ código de meio
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo tiver a capacidade de código de paficação ou se esse recurso for desconhecido; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_ \_ \_ número \_ de marcas do GETDEVCAPS do VCR MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o número de marcas (99).

</dd> <dt>

<span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>\_precisão de \_ busca do GETDEVCAPS VCR \_ MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a precisão de busca do dispositivo.

</dd> </dl>

Os sinalizadores a seguir podem ser especificados no membro **dwItem** dos [**\_ \_ parâmetros MCI GETDEVCAPS**](mci-getdevcaps-parms.md) para o tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>\_GETDEVCAPS MCI \_ OVLY \_ pode \_ congelar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder congelar a imagem; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>\_GETDEVCAPS MCI \_ OVLY \_ pode \_ alongar
</dt> <dd>

O membro **dwReturn** será definido como **true** se o dispositivo puder alongar a imagem para preencher o quadro; caso contrário, ele será definido como **false**.

</dd> <dt>

<span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI \_ OVLY \_ GETDEVCAPS \_ Max \_ Windows
</dt> <dd>

O membro **dwReturn** é definido como o número máximo de janelas que o dispositivo pode manipular simultaneamente.

</dd> </dl>

Os sinalizadores a seguir podem ser especificados no membro **dwItem** do [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para o tipo de dispositivo **VIDEODISC** :

<dl> <dt>

<span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>o MCI de \_ VD \_ GETDEVCAPS \_ pode \_ reverter
</dt> <dd>

O membro **dwReturn** será definido como **true** se o player do VIDEODISC puder reproduzir em ordem inversa; caso contrário, ele será definido como **false**. Alguns jogadores podem reproduzir discos CLV em discos inversos e CAV.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>\_cav de VD \_ GETDEVCAPS \_ MCI
</dt> <dd>

Quando combinado com outros itens, especifica que as informações de retorno se aplicam ao formato CAV videodiscs. Esse será o padrão se nenhum VIDEODISC for inserido.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>\_CLV de VD \_ GETDEVCAPS \_ MCI
</dt> <dd>

Quando combinado com outros itens, especifica que as informações de retorno se aplicam ao formato CLV videodiscs.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ \_ taxa rápida de VD GETDEVCAPS do MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a taxa de reprodução rápida padrão em quadros por segundo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>\_ \_ \_ taxa normal de VD GETDEVCAPS do MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a taxa de reprodução normal em quadros por segundo.

</dd> <dt>

<span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>\_ \_ taxa lenta de GETDEVCAPS de VD do \_ MCI \_
</dt> <dd>

O membro **dwReturn** é definido como a taxa de reprodução lenta padrão em quadros por segundo.

</dd> </dl>

Os sinalizadores a seguir podem ser especificados no membro **dwItem** do [**MCI \_ GETDEVCAPS \_ parms**](mci-getdevcaps-parms.md) para o tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_ \_ entrada GETDEVCAPS do Wave MCI \_
</dt> <dd>

O membro **dwReturn** é definido como o número total de dispositivos de entrada de onda (gravação).

</dd> <dt>

<span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>\_saída do \_ GETDEVCAPS \_ Wave MCI
</dt> <dd>

O membro **dwReturn** é definido como o número total de dispositivos de saída de onda (reprodução).

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
</dt> </dl>

 

