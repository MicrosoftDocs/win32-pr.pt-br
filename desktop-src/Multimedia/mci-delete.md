---
title: MCI_DELETE comando (mmsystem. h)
description: O \_ comando MCI Delete remove dados do arquivo. Os dispositivos digital-video e Wave-Audio reconhecem este comando.
ms.assetid: cf7fae86-e81e-4006-9755-fd01f81aeb62
keywords:
- MCI_DELETE comando Windows multimídia
topic_type:
- apiref
api_name:
- MCI_DELETE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada80894f9260d0c37323d645694e10b0bcef92e52ebd670764bb9a0c436f837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784576"
---
# <a name="mci_delete-command"></a>Comando de exclusão do MCI \_

O \_ comando MCI Delete remove dados do arquivo. Os dispositivos digital-video e Wave-Audio reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_DELETE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDelete
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

\_Notificação MCI, \_ espera MCI ou, para dispositivos de vídeo digital, teste MCI \_ . Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDelete"></span><span id="lpdelete"></span><span id="LPDELETE"></span>*lpDelete*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores se aplicam ao tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_DELETE_AT"></span><span id="mci_dgv_delete_at"></span>\_ \_ exclusão de DGV MCI \_ em
</dt> <dd>

Um retângulo é incluído no membro **RC** da estrutura identificada por *lpDelete*. O retângulo especifica a parte de cada quadro a ser excluída. Quando esse sinalizador é usado, o quadro é retido no espaço de trabalho e a área especificada pelo retângulo se torna preta. Se o sinalizador for omitido, o MCI \_ excluirá o padrão para o quadro inteiro e removerá o quadro do espaço de trabalho.

</dd> <dt>

<span id="MCI_DGV_DELETE_AUDIO_STREAM"></span><span id="mci_dgv_delete_audio_stream"></span>\_fluxo de \_ áudio de exclusão de DGV MCI \_ \_
</dt> <dd>

Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpDelete*. Se você usar esse sinalizador e também quiser excluir o vídeo, também deverá usar o sinalizador MCI \_ DGV \_ excluir \_ fluxo de vídeo \_ . (Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão excluídos.)

</dd> <dt>

<span id="MCI_DGV_DELETE_VIDEO_STREAM"></span><span id="mci_dgv_delete_video_stream"></span>\_fluxo de \_ vídeo de exclusão de DGV MCI \_ \_
</dt> <dd>

Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpDelete*. Se você usar esse sinalizador e também quiser excluir áudio, você também deverá usar o sinalizador de \_ fluxo de áudio MCI DGV \_ excluir \_ \_ . (Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão excluídos.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de
</dt> <dd>

Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpDelete*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Um local final é incluído no membro **dwTo** da estrutura identificada por *lpDelete*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do conjunto de MCI \_ .

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpDelete* aponta para uma estrutura de [**exclusão de \_ \_ \_ parâmetros DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_delete_parms) .

Os seguintes sinalizadores se aplicam ao tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de
</dt> <dd>

Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpDelete*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do [ \_ conjunto de MCI](mci-set.md).

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Um local final é incluído no membro **dwTo** da estrutura identificada por *lpDelete*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do conjunto de MCI \_ .

</dd> </dl>

Para dispositivos de formato de onda-áudio, o parâmetro *lpDelete* aponta para uma estrutura de [**parâmetros de \_ \_ exclusão \_ de Wave MCI**](mci-wave-delete-parms.md) .

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

 

