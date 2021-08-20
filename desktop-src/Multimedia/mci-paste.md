---
title: MCI_PASTE comando (Mmsystem.h)
description: O comando MCI \_ PASTE colará dados da área de transferência em um arquivo. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: cad5799a-08ef-4e34-803a-415b937d8fbd
keywords:
- MCI_PASTE comando Windows Multimídia
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
ms.openlocfilehash: 3bdc7b27838236b09952a009f1cb8c7d60091afb6634bbd74fad213f013f6e2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138227"
---
# <a name="mci_paste-command"></a>Comando MCI \_ PASTE

O comando MCI \_ PASTE colará dados da área de transferência em um arquivo. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT ou MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpPaste"></span><span id="lppaste"></span><span id="LPPASTE"></span>*lpPaste*
</dt> <dd>

Ponteiro para uma [**estrutura \_ MCI DGV \_ PASTE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_paste_parms)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_PASTE_AT"></span><span id="mci_dgv_paste_at"></span>MCI \_ DGV \_ COLAR \_ AT
</dt> <dd>

Um retângulo é incluído no **membro rc** da estrutura identificada por *lpPaste*. Os dois primeiros valores do retângulo especificam o ponto dentro do quadro para colocar as informações da área de transferência. Se a altura e a largura do retângulo não são zero, o conteúdo da área de transferência é dimensionado para essas dimensões quando elas são colar no quadro. Se o sinalizador for omitido, a MCI \_ PASTE assume como padrão todo o retângulo de quadro.

</dd> <dt>

<span id="MCI_DGV_PASTE_AUDIO_STREAM"></span><span id="mci_dgv_paste_audio_stream"></span>MCI \_ DGV \_ COLAR FLUXO DE \_ \_ ÁUDIO
</dt> <dd>

Um número de fluxo de áudio é incluído no **membro dwAudioStream** da estrutura identificada por *lpPaste*. Se houver apenas um fluxo de áudio na área de transferência, os dados de áudio serão gravados no fluxo designado. Se houver mais de um fluxo de áudio na área de transferência, o fluxo indicará o número inicial das sequências de fluxo. Se você usar esse sinalizador e também quiser colar vídeo, também deverá usar o sinalizador \_ MCI DGV \_ PASTE \_ VIDEO \_ STREAM. (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão gravados começando com o primeiro fluxo de áudio e vídeo. Cada fluxo colar retém seu número de fluxo original.)

</dd> <dt>

<span id="MCI_DGV_PASTE_INSERT"></span><span id="mci_dgv_paste_insert"></span>MCI \_ DGV \_ PASTE \_ INSERT
</dt> <dd>

Os dados da área de transferência devem ser inseridos no workspace existente na posição especificada pelo sinalizador MCI \_ TO. Todos os dados existentes após o ponto de inserção são movidos no workspace para tornar o espaço. Esse é o padrão.

</dd> <dt>

<span id="MCI_DGV_PASTE_OVERWRITE"></span><span id="mci_dgv_paste_overwrite"></span>MCI \_ DGV \_ PASTE \_ OVERWRITE
</dt> <dd>

Os dados da área de transferência devem substituir os dados já presentes no workspace. Os dados do workspace substituídos seguem o ponto de inserção.

</dd> <dt>

<span id="MCI_DGV_PASTE_VIDEO_STREAM"></span><span id="mci_dgv_paste_video_stream"></span>FLUXO DE VÍDEO \_ DE COLAR DGV \_ \_ da \_ MCI
</dt> <dd>

Um número de fluxo de vídeo é incluído no **membro dwVideoStream** da estrutura identificada por *lpPaste*. Se houver apenas um fluxo de vídeo na área de transferência, os dados de vídeo serão gravados no fluxo designado. Se houver mais de um fluxo de vídeo na área de transferência, o fluxo indicará o número inicial das sequências de fluxo. Se você usar esse sinalizador e também quiser colar áudio, também deverá usar o sinalizador \_ MCI DGV \_ PASTE \_ AUDIO \_ STREAM. (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão gravados começando com o primeiro fluxo de áudio e vídeo. Cada fluxo colar retém seu número de fluxo original.)

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ TO
</dt> <dd>

Um valor de posição é incluído no **membro dwTo** da estrutura identificada por *lpPaste*. O valor da posição especifica a posição para começar a colar dados no workspace. Se esse sinalizador for omitido, a posição assume como padrão a posição atual.

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

 

