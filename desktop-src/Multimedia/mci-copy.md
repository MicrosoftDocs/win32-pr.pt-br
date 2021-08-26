---
title: MCI_COPY comando (mmsystem. h)
description: O \_ comando de cópia MCI copia dados para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY comando Windows multimídia
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590acf61b352fa9abab00dfd49f3f54b166bfc340eaf12061e3d90b7a3025d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039286"
---
# <a name="mci_copy-command"></a>\_Comando de cópia MCI

O \_ comando de cópia MCI copia dados para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
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

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ \_ parâmetros de cópia DGV do MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_cópia DGV do MCI \_ \_ em
</dt> <dd>

Um retângulo é incluído no membro **RC** da estrutura identificada por *lpCopy*. O retângulo especifica a parte de cada quadro a ser copiada. Se o sinalizador for omitido, a \_ cópia do MCI copiará o quadro inteiro.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>\_fluxo de \_ áudio de cópia DGV \_ MCI \_
</dt> <dd>

Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpCopy*. Se você usar esse sinalizador e também quiser copiar o vídeo, também deverá usar o sinalizador de \_ fluxo de vídeo MCI DGV \_ Copy \_ \_ . (Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão copiados.)

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_fluxo de \_ vídeo de cópia DGV \_ MCI \_
</dt> <dd>

Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpCopy*. Se você usar esse sinalizador e também quiser copiar áudio, você também deverá usar o sinalizador de \_ fluxo de áudio MCI DGV \_ copiar \_ \_ . (Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão copiados.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de
</dt> <dd>

Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpCopy*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Um local final é incluído no membro **dwTo** da estrutura identificada por *lpCopy*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do \_ comando MCI set.

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

 

