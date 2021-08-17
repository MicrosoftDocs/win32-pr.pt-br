---
title: comando resume
description: O comando resume continua a reprodução ou gravação em um dispositivo que foi pausado usando o comando pause.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- retomar comando Windows Multimídia
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e4a728e3ca89e2b4ddc21809830d5af3be9a2b04e004f99d5a792a9be5da01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801888"
---
# <a name="resume-command"></a>comando resume

O comando resume continua a reprodução ou gravação em um dispositivo que foi pausado usando o [comando pause.](pause.md) Os dispositivos de vídeo digital, VCR e waveform-audio reconhecem esse comando. Embora os dispositivos de áudio CD, MIDI sequencer e videodisc também reconheçam esse comando, os drivers de dispositivo MCICDA, MCISEQ e MCIPIONR não são compatíveis com ele.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital e VCR, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="examples"></a>Exemplos

O comando a seguir continua a tocar ou gravar o dispositivo "newsound".

``` syntax
resume newsound
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[pause](pause.md)
</dt> </dl>

 

