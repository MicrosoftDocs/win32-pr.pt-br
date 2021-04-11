---
title: MCI_BREAK comando (mmsystem. h)
description: O \_ comando MCI Break define uma chave de interrupção para um dispositivo MCI. O MCI dá suporte a esse comando diretamente, em vez de passá-lo para o dispositivo. Qualquer aplicativo MCI pode usar esse comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- Multimídia do Windows de comando MCI_BREAK
topic_type:
- apiref
api_name:
- MCI_BREAK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33b17e3796192344ef974fed1af7229d41746aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454987"
---
# <a name="mci_break-command"></a>Comando de interrupção do MCI \_

O \_ comando MCI Break define uma chave de interrupção para um dispositivo MCI. O MCI dá suporte a esse comando diretamente, em vez de passá-lo para o dispositivo. Qualquer aplicativo MCI pode usar esse comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_BREAK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_BREAK_PARMS) lpBreak
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

\_Notificação MCI, espera de MCI \_ ou, para dispositivos de vídeo digital e gravador de fita de vídeo (VCR), \_ teste MCI. Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros de interrupção MCI**](mci-break-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Talvez seja necessário pressionar a tecla Break várias vezes para interromper uma operação de espera. Pressionar a tecla Break depois que uma espera de dispositivo é cancelada pode enviar a interrupção para um aplicativo. Se um aplicativo tiver uma ação definida para o código de chave virtual, ele poderá responder inadvertidamente à interrupção. Por exemplo, um aplicativo que usa VK \_ Cancel para uma tecla aceleradora pode responder à tecla Ctrl + Break padrão se for pressionado após a cancelamento de uma espera.

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos:

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>\_HWND de interrupção de MCI \_
</dt> <dd>

O membro **hwndBreak** da estrutura identificada por *lpBreak* contém um identificador de janela que deve ser a janela atual para habilitar a detecção de quebras para o dispositivo MCI. Normalmente, essa é a janela principal do aplicativo. Se omitido, o MCI não verificará o identificador de janela da janela atual.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>\_chave de interrupção MCI \_
</dt> <dd>

O membro **nVirtKey** da estrutura identificada por *lpBreak* especifica o código de chave virtual usado para a chave de interrupção. Por padrão, o MCI atribui CTRL + BREAK como a tecla Break. Esse sinalizador será necessário se a \_ interrupção do MCI \_ não for especificada.

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>interrupção do MCI \_ \_
</dt> <dd>

Desabilita qualquer chave de interrupção existente para o dispositivo indicado.

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

 

