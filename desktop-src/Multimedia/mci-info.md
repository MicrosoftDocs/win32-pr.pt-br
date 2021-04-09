---
title: MCI_INFO comando (mmsystem. h)
description: O \_ comando MCI info recupera informações de cadeia de caracteres de um dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- Multimídia do Windows de comando MCI_INFO
topic_type:
- apiref
api_name:
- MCI_INFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f6ba5be1c2a4ce94b880a87a468c594bc5b676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086232"
---
# <a name="mci_info-command"></a>Comando de informações do MCI \_

O \_ comando MCI info recupera informações de cadeia de caracteres de um dispositivo. Todos os dispositivos reconhecem este comando. As informações são retornadas no membro **lpstrReturn** da estrutura identificada por *lpInfo*. O membro **dwRetSize** especifica o tamanho do buffer para os dados retornados.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_INFO_PARMS) lpInfo
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

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros de informações MCI**](mci-info-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O seguinte sinalizador padrão adicional e específico de comando se aplica a todos os dispositivos que dão suporte a informações de MCI \_ :

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>\_produto de informações do MCI \_
</dt> <dd>

Obtém uma descrição do hardware associado a um dispositivo. Os dispositivos devem fornecer uma descrição que identifique o driver e o hardware usados.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **cdaudio** :

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>identidade de mídia do MCI \_ info \_ \_
</dt> <dd>

Produz um identificador exclusivo para o CD de áudio atualmente carregado no Player que está sendo consultado. Esse sinalizador retorna uma cadeia de 16 dígitos hexadecimais.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>informações do MCI \_ \_ mídia \_ UPC
</dt> <dd>

Produz o código do produto universal (UPC) que é codificado em um CD de áudio. O UPC é uma cadeia de caracteres de dígitos. Ele pode não estar disponível para todos os CDs.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>\_item de \_ informações do DGV MCI \_
</dt> <dd>

Uma constante que indica as informações desejadas é incluída no membro **dwItem** da estrutura identificada por *lpInfo*. As seguintes constantes são definidas para dispositivos de vídeo digital:

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>MCI \_ DGV \_ informações de \_ áudio \_ alg
</dt> <dd>

Retorna o nome do algoritmo de compactação de áudio atual.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>qualidade de áudio do MCI \_ DGV \_ info \_ \_
</dt> <dd>

Retorna o nome do descritor de qualidade de áudio atual.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>informações do MCI \_ DGV \_ ainda em \_ \_ alg
</dt> <dd>

Retorna o nome do algoritmo de compactação de imagem ainda atual.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>informações do MCI \_ DGV \_ \_ ainda \_ qualidade
</dt> <dd>

Retorna o nome do descritor de qualidade da imagem atual ainda.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>\_uso de \_ informações do DGV MCI \_
</dt> <dd>

Retorna uma cadeia de caracteres que descreve as restrições de uso que podem ser impostas pelo proprietário do Visual ou dos dados audíveis no espaço de trabalho.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>vídeo de informações do MCI \_ DGV \_ \_ \_ alg
</dt> <dd>

Retorna o nome do algoritmo de compactação de vídeo atual.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>\_qualidade de \_ vídeo de informações de DGV MCI \_ \_
</dt> <dd>

Retorna o nome do descritor de qualidade de vídeo atual.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>\_versão de informações do MCI \_
</dt> <dd>

Retorna o nível de versão do driver de dispositivo e do hardware. Os desenvolvedores de drivers de dispositivo devem documentar a sintaxe da cadeia de caracteres retornada.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>\_texto de \_ informações do DGV MCI \_
</dt> <dd>

Obtém a legenda da janela.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_arquivo de informações do MCI \_
</dt> <dd>

Obtém o caminho e o nome do último arquivo especificado com o comando [MCI \_ Open](mci-open.md) ou [MCI \_ Load](mci-load.md) . Se um arquivo não tiver sido especificado, o dispositivo retornará uma cadeia de caracteres terminada em nulo. Esse sinalizador tem suporte apenas em dispositivos que retornam **true** para o MCI \_ GETDEVCAPS \_ usa o \_ sinalizador de arquivos do comando [ \_ GETDEVCAPS do MCI](mci-getdevcaps.md) .

</dd> </dl>

Para dispositivos de vídeo digital, o *lpInfo* aponta para uma estrutura de parâmetros de [**informações de \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa) .

Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **Sequencer** :

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>informações de MCI \_ \_ direitos autorais
</dt> <dd>

Obtém o aviso de direitos autorais do arquivo MIDI do evento meta de direitos autorais.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_arquivo de informações do MCI \_
</dt> <dd>

Obtém o FileName do arquivo atual. Esse sinalizador tem suporte apenas em dispositivos que retornam **true** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o \_ GETDEVCAPS MCI que usa o \_ \_ sinalizador arquivos.

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>\_nome da informação MCI \_
</dt> <dd>

Obtém o nome da sequência do evento meta de nome de sequência/faixa.

</dd> </dl>

O seguinte sinalizador adicional se aplica ao tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>\_versão de \_ informações do VCR MCI \_
</dt> <dd>

Define o membro **lpstrReturn** da estrutura de [**parâmetros de \_ informações \_ do MCI**](mci-info-parms.md) para apontar para o número de versão. Também define o membro **dwRetSize** igual ao comprimento da cadeia de caracteres apontada para.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_arquivo de informações do MCI \_
</dt> <dd>

Obtém o FileName do arquivo atual. Esse sinalizador tem suporte apenas em dispositivos que retornam **true** para o MCI \_ GETDEVCAPS \_ usa o \_ sinalizador de arquivos do comando [ \_ GETDEVCAPS do MCI](mci-getdevcaps.md) .

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>\_texto de \_ informações do OVLY MCI \_
</dt> <dd>

Obtém a legenda da janela associada ao dispositivo de sobreposição de vídeo.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>\_arquivo de informações do MCI \_
</dt> <dd>

Obtém o FileName do arquivo atual. Esse sinalizador tem suporte de dispositivos que retornam **true** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o \_ GETDEVCAPS MCI \_ usando o \_ sinalizador arquivos.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda MCI \_
</dt> <dd>

Obtém o nome do produto da entrada atual.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_saída de onda MCI \_
</dt> <dd>

Obtém o nome do produto da saída atual e seu valor é específico do dispositivo.

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

 

