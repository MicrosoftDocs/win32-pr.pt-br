---
title: MCI_SIGNAL comando (mmsystem. h)
description: O \_ comando de sinal MCI define uma posição especificada no espaço de trabalho. Dispositivos de vídeo digital reconhecem este comando. O MCIAVI dá suporte a apenas um sinal ativo por vez.
ms.assetid: 32ca21a0-e2df-47f1-8e13-67c9d8f149db
keywords:
- Multimídia do Windows de comando MCI_SIGNAL
topic_type:
- apiref
api_name:
- MCI_SIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711238d73ee40f5809f15a2d6df93183fb17bf67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369525"
---
# <a name="mci_signal-command"></a>\_Comando de sinal MCI

O \_ comando de sinal MCI define uma posição especificada no espaço de trabalho. Dispositivos de vídeo digital reconhecem este comando. O MCIAVI dá suporte a apenas um sinal ativo por vez.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SIGNAL, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_SIGNAL_PARMS) lpSignal
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

<span id="lpSignal"></span><span id="lpsignal"></span><span id="LPSIGNAL"></span>*lpSignal*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ parâmetros de \_ sinal \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

A janela cujo identificador você especificar no membro **dwCallback** da estrutura de [**\_ parâmetros do \_ sinal \_ DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_signal_parms) recebe a mensagem mm \_ MCISIGNAL.

Os seguintes sinalizadores se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_SIGNAL_AT"></span><span id="mci_dgv_signal_at"></span>\_ \_ sinal de DGV MCI \_ em
</dt> <dd>

Uma posição de sinal é incluída no membro **dwPosition** da estrutura identificada por *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_CANCEL"></span><span id="mci_dgv_signal_cancel"></span>cancelamento de sinal MCI \_ DGV \_ \_
</dt> <dd>

Remove a posição do sinal especificada pelo valor associado ao \_ USERVAL do \_ sinal MCI DGV \_ .

</dd> <dt>

<span id="MCI_DGV_SIGNAL_EVERY"></span><span id="mci_dgv_signal_every"></span>\_sinal MCI DGV a \_ \_ cada
</dt> <dd>

Um valor de período de sinal é incluído no membro **dwPeriod** da estrutura identificada por *lpSignal*.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_POSITION"></span><span id="mci_dgv_signal_position"></span>\_posição do \_ sinal MCI DGV \_
</dt> <dd>

O dispositivo enviará o valor da posição com a mensagem do Windows em vez do valor especificado pelo usuário.

</dd> <dt>

<span id="MCI_DGV_SIGNAL_USERVAL"></span><span id="mci_dgv_signal_userval"></span>\_USERVAL do \_ sinal MCI DGV \_
</dt> <dd>

Um valor de dados é incluído no membro **dwUserParm** da estrutura identificada por *lpSignal*. O valor de dados associado a essa solicitação é relatado de volta com a mensagem do Windows.

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

 

