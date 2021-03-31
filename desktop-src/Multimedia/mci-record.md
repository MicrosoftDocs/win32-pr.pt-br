---
title: MCI_RECORD comando (mmsystem. h)
description: O \_ comando de registro MCI inicia a gravação a partir da posição atual ou de um local especificado para outro local especificado.
ms.assetid: d3c4e8a3-7d81-428e-91d8-d8d63fc0aa02
keywords:
- Multimídia do Windows de comando MCI_RECORD
topic_type:
- apiref
api_name:
- MCI_RECORD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cd15974753b8f40abd87b8d93622c090e2a57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085666"
---
# <a name="mci_record-command"></a>\_Comando de registro MCI

O comando de [**\_ registro MCI**](mci-record-parms.md) inicia a gravação a partir da posição atual ou de um local especificado para outro local especificado. Os dispositivos VCR e Wave-Audio reconhecem este comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RECORD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_RECORD_PARMS) lpRecord
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

<span id="lpRecord"></span><span id="lprecord"></span><span id="LPRECORD"></span>*lpRecord*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros de registro MCI**](mci-record-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Esse comando tem suporte em dispositivos que retornam **true** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o \_ GETDEVCAPS MCI \_ pode \_ gravar sinalizador. Para o driver MCIWAVE, todos os dados gravados após a abertura de um arquivo serão descartados se o arquivo for fechado sem salvá-lo.

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que dão suporte ao \_ registro MCI:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de
</dt> <dd>

Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpRecord*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) . Se \_ o MCI de não for especificado, o local inicial padrão será a posição atual.

</dd> <dt>

<span id="MCI_RECORD_INSERT"></span><span id="mci_record_insert"></span>\_inserção de registro de MCI \_
</dt> <dd>

As informações registradas recentemente devem ser inseridas ou coladas nos dados existentes. Alguns dispositivos podem não dar suporte a isso. Se houver suporte, esse será o padrão.

</dd> <dt>

<span id="MCI_RECORD_OVERWRITE"></span><span id="mci_record_overwrite"></span>\_substituição de registro de MCI \_
</dt> <dd>

Os dados devem substituir os dados existentes. O MCIWAVE. O dispositivo DRV retorna MCIERR \_ função sem suporte \_ em resposta a esse sinalizador.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Um local final é incluído no membro **dwTo** da estrutura identificada por *lpRecord*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) . Se \_ o MCI para não for especificado, o local final será padronizado para o final do conteúdo.

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_RECORD_AUDIO_STREAM"></span><span id="mci_dgv_record_audio_stream"></span>\_fluxo de \_ áudio de gravação de DGV MCI \_ \_
</dt> <dd>

Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpRecord*. Se você omitir esse sinalizador, os dados de áudio serão registrados no primeiro fluxo físico.

</dd> <dt>

<span id="MCI_DGV_RECORD_HOLD"></span><span id="mci_dgv_record_hold"></span>\_retenção de \_ registro de DGV MCI \_
</dt> <dd>

Quando a gravação for interrompida, a tela conterá a última imagem e não continuará mostrando o vídeo até que um comando de [ \_ Monitor MCI](mci-monitor.md) seja emitido.

</dd> <dt>

<span id="MCI_DGV_RECORD_VIDEO_STREAM"></span><span id="mci_dgv_record_video_stream"></span>\_fluxo de \_ vídeo de registro DGV \_ MCI \_
</dt> <dd>

Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpRecord*. Se você omitir esse sinalizador, os dados de vídeo serão registrados no primeiro fluxo físico.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect MCI
</dt> <dd>

Um retângulo é especificado no membro **RC** da estrutura identificada por *lpRecord*. O retângulo especifica a região da entrada externa usada como a origem dos pixels compactados e salvos. Esse retângulo assume como padrão o retângulo especificado (ou padronizado) pelo sinalizador de \_ vídeo MCI DGV \_ Put \_ para o comando [MCI \_ Put](mci-put.md) . Quando ele é definido de forma diferente do que o retângulo do vídeo, o que é exibido não é o que é gravado

</dd> </dl>

Para dispositivos de vídeo digital, o *lpRecord* aponta para uma estrutura de [**\_ \_ \_ parâmetros de registro DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_record_parms) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_RECORD_AT"></span><span id="mci_vcr_record_at"></span>\_ \_ registro de VCR MCI \_ em
</dt> <dd>

O membro **dwAt** da estrutura identificada por *lpRecord* contém uma hora em que o comando inteiro começa, ou se o dispositivo for cued, quando o dispositivo atingir a posição from fornecida pelo comando cue.

</dd> <dt>

<span id="MCI_VCR_RECORD_INITIALIZE"></span><span id="mci_vcr_record_initialize"></span>\_inicialização de \_ registro de VCR MCI \_
</dt> <dd>

Busque o dispositivo até o início da mídia, comece a gravar vídeo e áudio em branco e registre o código de ponto de inicio, se possível.

</dd> </dl>

Para dispositivos VCR, o *lpRecord* aponta para uma estrutura de parâmetros de [**registro de \_ VCR \_ \_ MCI**](mci-vcr-record-parms.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

