---
title: MCI_CUT comando (mmsystem. h)
description: O \_ comando Recortar do MCI remove os dados do arquivo e os copia para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- Multimídia do Windows de comando MCI_CUT
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918759"
---
# <a name="mci_cut-command"></a>\_Comando de recorte do MCI

O \_ comando Recortar do MCI remove os dados do arquivo e os copia para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
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

<span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*
</dt> <dd>

Ponteiro para uma estrutura [**MCI \_ DGV \_ recortar \_ parâmetros**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>DGV do MCI \_ \_ recortar \_ em
</dt> <dd>

Um retângulo é incluído no membro **RC** da estrutura identificada por *lpCut*. O retângulo especifica a parte de cada quadro a ser recortada. Se o sinalizador for omitido, o MCI \_ recortará o quadro inteiro.

</dd> <dt>

<span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>\_fluxo de \_ áudio de recorte MCI DGV \_ \_
</dt> <dd>

Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpCut*. Se você usar esse sinalizador e também quiser recortar o vídeo, também deverá usar o \_ sinalizador de \_ fluxo de vídeo de recorte do DGV MCI \_ \_ . (Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão recortados.)

</dd> <dt>

<span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_fluxo de \_ vídeo de recorte de DGV MCI \_ \_
</dt> <dd>

Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpCut*. Se você usar esse sinalizador e também quiser cortar o áudio, também deverá usar o sinalizador de \_ \_ fluxo de áudio de recorte MCI DGV \_ \_ . (Se nenhum sinalizador for especificado, os dados de todos os fluxos de áudio e vídeo serão recortados.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de
</dt> <dd>

Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpCut*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Um local final é incluído no membro **dwTo** da estrutura identificada por *lpCut*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do conjunto de MCI \_ .

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

 

