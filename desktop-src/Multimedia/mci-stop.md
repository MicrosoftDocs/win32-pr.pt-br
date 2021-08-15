---
title: MCI_STOP comando (Mmsystem.h)
description: O comando MCI STOP interrompe todas as sequências de reprodução e gravação, descarrega todos os buffers de reprodução e interrompe \_ a exibição de imagens de vídeo. Os dispositivos de áudio cd, vídeo digital, sequenciador MIDI, videodisc, VCR e waveform-audio reconhecem esse comando.
ms.assetid: e5ae20b3-7439-4314-8354-d06e83b29729
keywords:
- MCI_STOP comando Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_STOP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02830dde544e025447cb72df6ff3720857985384ff6bd074c5e0718b114697c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374598"
---
# <a name="mci_stop-command"></a>Comando MCI \_ STOP

O comando MCI STOP interrompe todas as sequências de reprodução e gravação, descarrega todos os buffers de reprodução e interrompe \_ a exibição de imagens de vídeo. Os dispositivos de áudio cd, vídeo digital, sequenciador MIDI, videodisc, VCR e waveform-audio reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STOP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStop
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

<span id="lpStop"></span><span id="lpstop"></span><span id="LPSTOP"></span>*lpStop*
</dt> <dd>

Ponteiro para uma [**estrutura \_ \_ PARMS GENÉRICA da MCI.**](mci-generic-parms.md) (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

A diferença entre os comandos MCI \_ STOP e [MCI \_ PAUSE](mci-pause.md) depende do dispositivo. Se possível, a MCI \_ PAUSE suspende a operação do dispositivo, mas deixa o dispositivo pronto para retomar a reprodução imediatamente.

Para o dispositivo de áudio CD, o MCI STOP redefine a posição atual da faixa como zero; por outro \_ lado, [a MCI \_ PAUSE](mci-pause.md) mantém a posição atual da faixa, prevendo que o dispositivo retomará a reprodução.

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

 

