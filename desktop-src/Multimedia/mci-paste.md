---
title: MCI_PASTE comando (mmsystem. h)
description: O \_ comando Paste do MCI cola os dados da área de transferência em um arquivo. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- Multimídia do Windows de comando MCI_PASTE
topic_type:
- apiref
api_name:
- MCI_PASTE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b15ff0ae3d14c1df63fbd9ab0c93a85446bdf066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644231"
---
# <a name="mci_paste-command"></a>\_Comando de colar MCI

O \_ comando Paste do MCI cola os dados da área de transferência em um arquivo. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PASTE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_PASTE_PARMS) lpPaste
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

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ parâmetros de \_ colagem \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>\_colar DGV do MCI \_ \_ em
</dt> <dd>

Um retângulo é incluído no membro **RC** da estrutura identificada por *lpPaste*. Os dois primeiros valores do retângulo especificam o ponto dentro do quadro para inserir as informações da área de transferência. Se a altura e a largura do retângulo forem diferentes de zero, o conteúdo da área de transferência será dimensionado para essas dimensões quando elas forem coladas no quadro. Se o sinalizador for omitido, a \_ colagem do MCI padronizará para todo o retângulo do quadro.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>fluxo de áudio do MCI \_ DGV \_ colar \_ \_
</dt> <dd>

Um número de fluxo de áudio é incluído no membro **dwAudioStream** da estrutura identificada por *lpPaste*. Se houver apenas um fluxo de áudio na área de transferência, os dados de áudio serão colados no fluxo designado. Se houver mais de um fluxo de áudio na área de transferência, o fluxo indicará o número inicial para as sequências de fluxo. Se você usar esse sinalizador e também quiser colar o vídeo, você também deverá usar o sinalizador de fluxo de vídeo MCI do \_ DGV de \_ colagem \_ \_ . (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão colados começando com o primeiro fluxo de áudio e vídeo. Cada fluxo colado mantém seu número de fluxo original.)

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>\_inserção de \_ colar \_ DGV MCI
</dt> <dd>

Os dados da área de transferência devem ser inseridos no espaço de trabalho existente na posição especificada pelo \_ sinalizador MCI. Todos os dados existentes após o ponto de inserção são movidos no espaço de trabalho para liberar espaço. Esse é o padrão.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>\_substituição de \_ colar \_ DGV MCI
</dt> <dd>

Os dados da área de transferência devem substituir os dados já presentes no espaço de trabalho. Os dados de espaço de trabalho substituídos seguem o ponto de inserção.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>\_fluxo de \_ vídeo de colar DGV \_ MCI \_
</dt> <dd>

Um número de fluxo de vídeo é incluído no membro **dwVideoStream** da estrutura identificada por *lpPaste*. Se houver apenas um fluxo de vídeo na área de transferência, os dados de vídeo serão colados no fluxo designado. Se houver mais de um fluxo de vídeo na área de transferência, o fluxo indicará o número inicial para as sequências de fluxo. Se você usar esse sinalizador e também quiser colar o áudio, também deverá usar o sinalizador de \_ fluxo de áudio MCI DGV \_ colar \_ \_ . (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão colados começando com o primeiro fluxo de áudio e vídeo. Cada fluxo colado mantém seu número de fluxo original.)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Um valor de posição é incluído no membro **dwTo** da estrutura identificada por *lpPaste*. O valor de posição especifica a posição para começar a colar dados no espaço de trabalho. Se esse sinalizador for omitido, a posição padrão será a posição atual.

</dd> </dl>

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

 

