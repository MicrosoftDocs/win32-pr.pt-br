---
title: MCI_BREAK comando (Mmsystem.h)
description: O comando MCI \_ BREAK define uma chave de quebra para um dispositivo MCI. A MCI dá suporte a esse comando diretamente em vez de passá-lo para o dispositivo. Qualquer aplicativo MCI pode usar esse comando.
ms.assetid: 127b5179-2838-4bde-8d0c-37a4cc87fa4d
keywords:
- MCI_BREAK comando Windows Multimídia
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
ms.openlocfilehash: 07006ddfb38e1a57f6e08cb73d9b33021d139b9542245aec137e0969378140e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803958"
---
# <a name="mci_break-command"></a>Comando MCI \_ BREAK

O comando MCI \_ BREAK define uma chave de quebra para um dispositivo MCI. A MCI dá suporte a esse comando diretamente em vez de passá-lo para o dispositivo. Qualquer aplicativo MCI pode usar esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI NOTIFY, MCI WAIT ou, para dispositivos VCR (gravador de gravação de vídeo \_ \_ e vídeo), MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpBreak"></span><span id="lpbreak"></span><span id="LPBREAK"></span>*lpBreak*
</dt> <dd>

Ponteiro para uma [**estrutura MCI \_ BREAK \_ PARMS.**](mci-break-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Talvez seja preciso pressionar a tecla break várias vezes para interromper uma operação de espera. Pressionar a tecla de quebra depois que uma espera do dispositivo for cancelada pode enviar a quebra para um aplicativo. Se um aplicativo tiver uma ação definida para o código de chave virtual, ele poderá responder inadvertidamente à quebra. Por exemplo, um aplicativo que usa CANCEL da VK para uma tecla de acelerador pode responder à tecla CTRL+BREAK padrão se ela for pressionada depois que uma espera \_ for cancelada.

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos:

<dl> <dt>

<span id="MCI_BREAK_HWND"></span><span id="mci_break_hwnd"></span>MCI \_ BREAK \_ HWND
</dt> <dd>

O **membro hwndBreak** da estrutura identificada por *lpBreak* contém um identificador de janela que deve ser a janela atual para habilitar a detecção de quebra para esse dispositivo MCI. Essa geralmente é a janela principal do aplicativo. Se omitido, a MCI não verifica o alça de janela da janela atual.

</dd> <dt>

<span id="MCI_BREAK_KEY"></span><span id="mci_break_key"></span>CHAVE DE QUEBRA DA MCI \_ \_
</dt> <dd>

O **membro nVirtKey** da estrutura identificada por *lpBreak* especifica o código de chave virtual usado para a chave de quebra. Por padrão, a MCI atribui CTRL+BREAK como a chave de quebra. Esse sinalizador será necessário se MCI \_ BREAK OFF não for \_ especificado.

</dd> <dt>

<span id="MCI_BREAK_OFF"></span><span id="mci_break_off"></span>MCI \_ BREAK \_ OFF
</dt> <dd>

Desabilita qualquer chave de quebra existente para o dispositivo indicado.

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

 

