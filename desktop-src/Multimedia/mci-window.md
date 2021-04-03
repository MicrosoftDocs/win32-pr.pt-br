---
title: MCI_WINDOW comando (mmsystem. h)
description: O \_ comando da janela MCI especifica a janela e as características da janela para dispositivos gráficos. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- Multimídia do Windows de comando MCI_WINDOW
topic_type:
- apiref
api_name:
- MCI_WINDOW
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b4d630dbc9dbc7403e93cd0bda3de2eef1e5cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918595"
---
# <a name="mci_window-command"></a>\_Comando de janela MCI

O \_ comando da janela MCI especifica a janela e as características da janela para dispositivos gráficos. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WINDOW, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpWindow
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

\_Notificação MCI, \_ espera MCI ou, para dispositivos de vídeo digital, teste MCI \_ . Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os dispositivos gráficos devem criar uma janela padrão quando um dispositivo é aberto, mas não deve exibi-la até receber o comando [MCI \_ Play](mci-play.md) . O \_ comando da janela MCI é usado para fornecer uma janela criada pelo aplicativo ao dispositivo e alterar as características de exibição de uma janela de exibição padrão ou definida pelo aplicativo. Se o aplicativo fornecer a janela de exibição, ele deverá estar preparado para atualizar um retângulo inválido na janela.

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>\_HWND de \_ janela \_ DGV MCI
</dt> <dd>

O identificador da janela necessária para uso como destino é incluído no membro **HWND** da estrutura identificada por *lpWindow*.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>\_estado da \_ janela MCI DGV \_
</dt> <dd>

O membro **nCmdShow** da estrutura identificada por *lpWindow* contém parâmetros para definir o estado da janela.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>\_texto da \_ janela MCI DGV \_
</dt> <dd>

O membro **lpstrText** da estrutura identificada por *lpWindow* contém um endereço de um buffer que contém a legenda usada na barra de título da janela.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpWindow* aponta para uma estrutura de [**\_ \_ \_ parâmetros de janela DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>janela do MCI \_ OVLY \_ \_ desabilitar \_ Stretch
</dt> <dd>

Desabilita o alongamento da imagem.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>\_janela MCI \_ OVLY \_ habilitar \_ Stretch
</dt> <dd>

Habilita o alongamento da imagem.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>\_HWND de \_ janela \_ OVLY MCI
</dt> <dd>

O identificador da janela usada para o destino é incluído no membro **HWND** da estrutura identificada por *lpWindow*. Defina esse sinalizador como \_ \_ padrão da janela MCI OVLY \_ para retornar à janela padrão.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>\_estado da \_ janela MCI OVLY \_
</dt> <dd>

O membro **nCmdShow** da estrutura *lpWindow* contém parâmetros para definir o estado da janela. Esse sinalizador é equivalente a chamar a ação de [janela](/windows/win32/api/winuser/nf-winuser-showwindow) com o parâmetro *State* . As constantes são as mesmas definidas no WINDOWS. H (por exemplo \_ , ocultar SW, SW \_ minimize ou SW \_ normal).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>\_texto da \_ janela MCI OVLY \_
</dt> <dd>

O membro **lpstrText** da estrutura identificada por *lpWindow* contém um endereço de um buffer que contém a legenda usada para a janela.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, o parâmetro *lpWindow* aponta para uma estrutura de [**\_ \_ \_ parâmetros de janela OVLY MCI**](mci-ovly-window-parms.md) .

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

 

