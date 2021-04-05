---
title: MCI_SEEK comando (mmsystem. h)
description: O \_ comando MCI Seek altera a posição atual no conteúdo o mais rápido possível.
ms.assetid: 5ffab964-a28d-4dc2-ac04-da501cd34d24
keywords:
- Multimídia do Windows de comando MCI_SEEK
topic_type:
- apiref
api_name:
- MCI_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e34f6fa823092968e74515a885e7a40db9f2d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009057"
---
# <a name="mci_seek-command"></a>Comando de busca do MCI \_

O \_ comando MCI Seek altera a posição atual no conteúdo o mais rápido possível. A saída de vídeo e áudio é desabilitada durante a busca. Depois que a busca for concluída, o dispositivo será interrompido. CD de áudio, digital-vídeo, MIDI Sequencer, VCR, VIDEODISC e formato de onda-os dispositivos de áudio reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SEEK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SEEK_PARMS) lpSeek
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

<span id="lpSeek"></span><span id="lpseek"></span><span id="LPSEEK"></span>*lpSeek*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros de busca MCI**](mci-seek-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Se um tamanho de amostra de dados para um dispositivo for maior do que 1 byte (como com dados de wave-áudio estéreo), esse comando passará para o início do exemplo mais próximo quando uma posição especificada não coincidir com o início de um exemplo.

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que dão suporte ao MCI \_ Seek:

<dl> <dt>

<span id="MCI_SEEK_TO_END"></span><span id="mci_seek_to_end"></span>MCI \_ buscar \_ até o \_ fim
</dt> <dd>

Busque até o final do conteúdo.

</dd> <dt>

<span id="MCI_SEEK_TO_START"></span><span id="mci_seek_to_start"></span>MCI \_ buscar \_ para \_ Iniciar
</dt> <dd>

Procure o início do conteúdo.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Uma posição é incluída no membro **dwTo** da estrutura identificada por *lpSeek*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) . Não use esse sinalizador com o MCI \_ Seek \_ para \_ final ou MCI \_ Seek \_ para \_ Iniciar.

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_SEEK_AT"></span><span id="mci_vcr_seek_at"></span>o \_ VCR do MCI \_ busca \_ em
</dt> <dd>

O membro **dwAt** da estrutura identificada por *lpSeek* contém uma hora em que o comando inteiro começa.

</dd> <dt>

<span id="MCI_VCR_SEEK_MARK"></span><span id="mci_vcr_seek_mark"></span>\_marca de \_ busca do VCR MCI \_
</dt> <dd>

O membro **dwMark** da estrutura identificada por *lpSeek* contém a marca numerada a ser pesquisada.

</dd> <dt>

<span id="MCI_VCR_SEEK_REVERSE"></span><span id="mci_vcr_seek_reverse"></span>inverso de busca de videocassete de MCI \_ \_ \_
</dt> <dd>

A direção de busca é inversa; Isso é usado apenas com o \_ sinalizador de marca de busca de VCR MCI \_ \_ .

</dd> </dl>

Para dispositivos VCR, o parâmetro *lpSeek* aponta para uma estrutura de parâmetros de busca de videocassete do [**MCI \_ \_ \_**](mci-vcr-seek-parms.md) .

O seguinte sinalizador adicional é usado com o tipo de dispositivo **VIDEODISC** :

<dl> <dt>

<span id="MCI_VD_SEEK_REVERSE"></span><span id="mci_vd_seek_reverse"></span>\_inversa de \_ busca de VD do MCI \_
</dt> <dd>

A direção de busca é inversa.

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

 

