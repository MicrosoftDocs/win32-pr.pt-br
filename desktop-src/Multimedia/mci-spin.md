---
title: MCI_SPIN comando (Mmsystem.h)
description: O comando SPIN da MCI \_ inicia a rotação do dispositivo para cima ou para baixo. Os dispositivos Videodisc reconhecem esse comando.
ms.assetid: 9e491455-d06d-44c6-8aca-6360384ec266
keywords:
- MCI_SPIN comando Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_SPIN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41457cbd04de7ffc85248912224819f9c7549c8aebd34d60c4a7efcd70bbcada
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374588"
---
# <a name="mci_spin-command"></a>Comando SPIN da \_ MCI

O comando SPIN da MCI \_ inicia a rotação do dispositivo para cima ou para baixo. Os dispositivos Videodisc reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SPIN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSpin
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

MCI \_ NOTIFY ou MCI \_ WAIT. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpSpin"></span><span id="lpspin"></span><span id="LPSPIN"></span>*lpSpin*
</dt> <dd>

Ponteiro para uma [**estrutura \_ \_ PARMS GENÉRICA da MCI.**](mci-generic-parms.md) (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a dispositivos videodisc:

<dl> <dt>

<span id="MCI_VD_SPIN_DOWN"></span><span id="mci_vd_spin_down"></span>ROTAÇÃO \_ PARA BAIXO da VD \_ da MCI \_
</dt> <dd>

Interrompe a rotação do disco.

</dd> <dt>

<span id="MCI_VD_SPIN_UP"></span><span id="mci_vd_spin_up"></span>MCI \_ VD \_ SPIN \_ UP
</dt> <dd>

Inicia a rotação do disco.

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

 

