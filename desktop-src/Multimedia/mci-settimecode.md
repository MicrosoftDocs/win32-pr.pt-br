---
title: MCI_SETTIMECODE comando (mmsystem. h)
description: O \_ comando MCI SetCode habilita ou desabilita a gravação do código de paficação de um videocassete. Os dispositivos VCR reconhecem este comando.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- Multimídia do Windows de comando MCI_SETTIMECODE
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759365"
---
# <a name="mci_settimecode-command"></a>Comando do MCI \_ SETcode

O \_ comando MCI SetCode habilita ou desabilita a gravação do código de paficação de um videocassete. Os dispositivos VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
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

<span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O seguinte sinalizador adicional se aplica a dispositivos VCR:

<dl> <dt>

<span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_registro SETcode-of-código de VCR MCI \_ \_
</dt> <dd>

Define a gravação de controle de código de Code como on ou off. Esse sinalizador é usado em combinação com um dos seguintes sinalizadores adicionais:

</dd> <dt>

<span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ definido \_ em
</dt> <dd>

Gravação de código de ponto em.

</dd> <dt>

<span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>conjunto de MCI \_ \_ desativado
</dt> <dd>

Gravação de código de ponto desativada.

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

 

