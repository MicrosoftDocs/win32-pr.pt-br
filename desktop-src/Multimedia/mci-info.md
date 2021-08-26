---
title: MCI_INFO comando (Mmsystem.h)
description: O comando MCI \_ INFO recupera informações de cadeia de caracteres de um dispositivo.
ms.assetid: aed3fed3-87b9-4673-9171-4f57770d765c
keywords:
- MCI_INFO comando Windows Multimídia
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
ms.openlocfilehash: 18d53acbdfeb0c13b4b9e201d1bea23008dfbaa83221007152181fe685d09957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039195"
---
# <a name="mci_info-command"></a>Comando MCI \_ INFO

O comando MCI \_ INFO recupera informações de cadeia de caracteres de um dispositivo. Todos os dispositivos reconhecem esse comando. As informações são retornadas **no membro lpstrReturn** da estrutura identificada por *lpInfo.* O **membro dwRetSize** especifica o comprimento do buffer para os dados retornados.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI WAIT ou, para dispositivos de vídeo digital e \_ VCR, MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpInfo"></span><span id="lpinfo"></span><span id="LPINFO"></span>*lpInfo*
</dt> <dd>

Ponteiro para uma [**estrutura MCI \_ INFO \_ PARMS.**](mci-info-parms.md) (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

O seguinte sinalizador padrão adicional e específico de comando se aplica a todos os dispositivos que suportam INFORMAÇÕES de \_ MCI:

<dl> <dt>

<span id="MCI_INFO_PRODUCT"></span><span id="mci_info_product"></span>PRODUTO DE INFORMAÇÕES DA MCI \_ \_
</dt> <dd>

Obtém uma descrição do hardware associado a um dispositivo. Os dispositivos devem fornecer uma descrição que identifique o driver e o hardware usado.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam ao **tipo de dispositivo cdaudio:**

<dl> <dt>

<span id="MCI_INFO_MEDIA_IDENTITY"></span><span id="mci_info_media_identity"></span>IDENTIDADE DE MÍDIA \_ DE \_ INFORMAÇÕES DA \_ MCI
</dt> <dd>

Produz um identificador exclusivo para o CD de áudio carregado atualmente no player que está sendo consultado. Esse sinalizador retorna uma cadeia de caracteres de 16 dígitos hexadecimais.

</dd> <dt>

<span id="MCI_INFO_MEDIA_UPC"></span><span id="mci_info_media_upc"></span>UPC DE \_ \_ MÍDIA DE INFORMAÇÕES \_ DA MCI
</dt> <dd>

Produz o UPC (Código do Produto Universal) codificado em um CD de áudio. O UPC é uma cadeia de caracteres de dígitos. Ele pode não estar disponível para todos os CDs.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam ao **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_INFO_ITEM"></span><span id="mci_dgv_info_item"></span>ITEM DE \_ INFORMAÇÕES DE DGV \_ da MCI \_
</dt> <dd>

Uma constante que indica as informações desejadas está incluída no **membro dwItem** da estrutura identificada por *lpInfo*. As seguintes constantes são definidas para dispositivos de vídeo digital:

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_ALG"></span><span id="mci_dgv_info_audio_alg"></span>ALG DE ÁUDIO DE INFORMAÇÕES DE \_ DGV \_ \_ \_ da MCI
</dt> <dd>

Retorna o nome do algoritmo de compactação de áudio atual.

</dd> <dt>

<span id="MCI_DGV_INFO_AUDIO_QUALITY"></span><span id="mci_dgv_info_audio_quality"></span>QUALIDADE DE ÁUDIO \_ DE INFORMAÇÕES DE DGV \_ \_ da \_ MCI
</dt> <dd>

Retorna o nome do descritor de qualidade de áudio atual.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_ALG"></span><span id="mci_dgv_info_still_alg"></span>INFORMAÇÕES \_ DE DGV DA MCI \_ \_ AINDA SÃO \_ ALG
</dt> <dd>

Retorna o nome do algoritmo de compactação de imagem ainda atual.

</dd> <dt>

<span id="MCI_DGV_INFO_STILL_QUALITY"></span><span id="mci_dgv_info_still_quality"></span>QUALIDADE AINDA \_ DAS INFORMAÇÕES DE DGV DA MCI \_ \_ \_
</dt> <dd>

Retorna o nome do descritor de qualidade da imagem ainda atual.

</dd> <dt>

<span id="MCI_DGV_INFO_USAGE"></span><span id="mci_dgv_info_usage"></span>USO DE \_ INFORMAÇÕES DE DGV \_ da MCI \_
</dt> <dd>

Retorna uma cadeia de caracteres que descreve as restrições de uso que podem ser impostas pelo proprietário dos dados visuais ou audíveis no workspace.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_ALG"></span><span id="mci_dgv_info_video_alg"></span>ALG DE VÍDEO DE INFORMAÇÕES DE \_ DGV \_ \_ \_ DA MCI
</dt> <dd>

Retorna o nome do algoritmo de compactação de vídeo atual.

</dd> <dt>

<span id="MCI_DGV_INFO_VIDEO_QUALITY"></span><span id="mci_dgv_info_video_quality"></span>QUALIDADE DO VÍDEO DE INFORMAÇÕES \_ DE DGV \_ \_ DA \_ MCI
</dt> <dd>

Retorna o nome do descritor de qualidade de vídeo atual.

</dd> <dt>

<span id="MCI_INFO_VERSION"></span><span id="mci_info_version"></span>VERSÃO DE INFORMAÇÕES DA MCI \_ \_
</dt> <dd>

Retorna o nível de versão do driver e do hardware do dispositivo. Os desenvolvedores de driver de dispositivo devem documentar a sintaxe da cadeia de caracteres retornada.

</dd> <dt>

<span id="MCI_DGV_INFO_TEXT"></span><span id="mci_dgv_info_text"></span>TEXTO DE \_ INFORMAÇÕES DE DGV \_ da MCI \_
</dt> <dd>

Obtém a legenda da janela.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>ARQUIVO DE INFORMAÇÕES DA MCI \_ \_
</dt> <dd>

Obtém o caminho e o nome do arquivo do último arquivo especificado com o [comando MCI \_ OPEN](mci-open.md) ou [MCI \_ LOAD.](mci-load.md) Se um arquivo não tiver sido especificado, o dispositivo retornará uma cadeia de caracteres terminada em nulo. Esse sinalizador só tem suporte em dispositivos que **retornam TRUE** para o sinalizador MCI \_ GETDEVCAPS USES FILES do \_ comando \_ [MCI \_ GETDEVCAPS.](mci-getdevcaps.md)

</dd> </dl>

Para dispositivos de vídeo digital, *lpInfo* aponta para uma estrutura [**\_ MCI DGV \_ INFO \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_info_parmsa)

Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **sequencer:**

<dl> <dt>

<span id="MCI_INFO_COPYRIGHT"></span><span id="mci_info_copyright"></span>DIREITOS \_ AUTORAIS DE INFORMAÇÕES DA MCI \_
</dt> <dd>

Obtém a notificação de direitos autorais do arquivo MIDI do meta evento de direitos autorais.

</dd> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>ARQUIVO DE INFORMAÇÕES DA MCI \_ \_
</dt> <dd>

Obtém o nome do arquivo atual. Esse sinalizador só é compatível com dispositivos que retornam **TRUE** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o sinalizador \_ MCI GETDEVCAPS \_ USES \_ FILES.

</dd> <dt>

<span id="MCI_INFO_NAME"></span><span id="mci_info_name"></span>NOME DAS INFORMAÇÕES DA MCI \_ \_
</dt> <dd>

Obtém o nome da sequência do metadado de nome de sequência/faixa.

</dd> </dl>

O seguinte sinalizador adicional se aplica ao tipo **de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_INFO_VERSION"></span><span id="mci_vcr_info_version"></span>VERSÃO DE \_ INFORMAÇÕES DO VCR \_ da MCI \_
</dt> <dd>

Define **o membro lpstrReturn** da estrutura [**MCI INFO \_ \_ PARMS**](mci-info-parms.md) para apontar para o número de versão. Também define o **membro dwRetSize** igual ao comprimento da cadeia de caracteres apontada.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam ao tipo **de dispositivo de sobreposição:**

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>ARQUIVO DE INFORMAÇÕES DA MCI \_ \_
</dt> <dd>

Obtém o nome do arquivo atual. Esse sinalizador só tem suporte em dispositivos que **retornam TRUE** para o sinalizador MCI \_ GETDEVCAPS USES FILES do \_ comando \_ [MCI \_ GETDEVCAPS.](mci-getdevcaps.md)

</dd> <dt>

<span id="MCI_OVLY_INFO_TEXT"></span><span id="mci_ovly_info_text"></span>TEXTO DE INFORMAÇÕES DO MCI \_ OVLY \_ \_
</dt> <dd>

Obtém a legenda da janela associada ao dispositivo de sobreposição de vídeo.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam ao tipo **de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_INFO_FILE"></span><span id="mci_info_file"></span>ARQUIVO DE INFORMAÇÕES DA MCI \_ \_
</dt> <dd>

Obtém o nome do arquivo atual. Esse sinalizador é compatível com dispositivos que retornam **TRUE** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o sinalizador \_ MCI GETDEVCAPS \_ USES \_ FILES.

</dd> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>ENTRADA DE ONDA MCI \_ \_
</dt> <dd>

Obtém o nome do produto da entrada atual.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>SAÍDA DE ONDA DA MCI \_ \_
</dt> <dd>

Obtém o nome do produto da saída atual e seu valor é específico do dispositivo.

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

 

