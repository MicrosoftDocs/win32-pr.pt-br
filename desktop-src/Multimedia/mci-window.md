---
title: MCI_WINDOW comando (Mmsystem.h)
description: O comando MCI \_ WINDOW especifica a janela e as características da janela para dispositivos gráficos. Os dispositivos de vídeo digital e de sobreposição de vídeo reconhecem esse comando.
ms.assetid: 8b6c4d9a-ee72-4c64-aebe-6c8153167496
keywords:
- MCI_WINDOW comando Windows Multimídia
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
ms.openlocfilehash: 3270dce8b2127cce783c7c3b8bf21102590cd3e82d74a3e990a3117c59772381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783686"
---
# <a name="mci_window-command"></a>Comando MCI \_ WINDOW

O comando MCI \_ WINDOW especifica a janela e as características da janela para dispositivos gráficos. Os dispositivos de vídeo digital e de sobreposição de vídeo reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT ou, para dispositivos de vídeo digital, MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpWindow"></span><span id="lpwindow"></span><span id="LPWINDOW"></span>*lpWindow*
</dt> <dd>

Ponteiro para uma [**estrutura \_ \_ PARMS GENÉRICA da MCI.**](mci-generic-parms.md) (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Os dispositivos gráficos devem criar uma janela padrão quando um dispositivo é aberto, mas não devem exibi-la até que recebam o [comando MCI \_ PLAY.](mci-play.md) O comando WINDOW da MCI é usado para fornecer uma janela criada pelo aplicativo para o dispositivo e alterar as características de exibição de uma janela de exibição padrão ou definida \_ pelo aplicativo. Se o aplicativo fornece a janela de exibição, ele deve estar preparado para atualizar um retângulo inválido na janela.

Os seguintes sinalizadores adicionais são usados com o **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_WINDOW_HWND"></span><span id="mci_dgv_window_hwnd"></span>HWND DA JANELA \_ DGV \_ \_ da MCI
</dt> <dd>

O identificador da janela necessária para uso como destino está incluído no **membro hWnd** da estrutura identificada por *lpWindow*.

</dd> <dt>

<span id="MCI_DGV_WINDOW_STATE"></span><span id="mci_dgv_window_state"></span>ESTADO DA \_ JANELA DGV \_ da MCI \_
</dt> <dd>

O **membro nCmdShow** da estrutura identificada por *lpWindow* contém parâmetros para definir o estado da janela.

</dd> <dt>

<span id="MCI_DGV_WINDOW_TEXT"></span><span id="mci_dgv_window_text"></span>TEXTO DA \_ JANELA DGV \_ da MCI \_
</dt> <dd>

O **membro lpstrText** da estrutura identificada por *lpWindow* contém um endereço de um buffer que contém a legenda usada na barra de título da janela.

</dd> </dl>

Para dispositivos de vídeo digital, o *parâmetro lpWindow* aponta para uma estrutura [**\_ MCI DGV \_ WINDOW \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_window_parmsa)

Os seguintes sinalizadores adicionais são usados com o tipo **de dispositivo de sobreposição:**

<dl> <dt>

<span id="MCI_OVLY_WINDOW_DISABLE_STRETCH"></span><span id="mci_ovly_window_disable_stretch"></span>JANELA DO MCI \_ OVLY \_ \_ DESABILITAR \_ STRETCH
</dt> <dd>

Desabilita o alongamento da imagem.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_ENABLE_STRETCH"></span><span id="mci_ovly_window_enable_stretch"></span>MCI \_ OVLY \_ WINDOW \_ ENABLE \_ STRETCH
</dt> <dd>

Habilita o alongamento da imagem.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_HWND"></span><span id="mci_ovly_window_hwnd"></span>MCI \_ OVLY \_ WINDOW \_ HWND
</dt> <dd>

O identificador da janela usada para o destino é incluído no **membro hWnd** da estrutura identificada por *lpWindow*. Demarque esse sinalizador como MCI \_ OVLY \_ WINDOW DEFAULT para retornar à janela \_ padrão.

</dd> <dt>

<span id="MCI_OVLY_WINDOW_STATE"></span><span id="mci_ovly_window_state"></span>ESTADO DA \_ JANELA OVLY \_ DA MCI \_
</dt> <dd>

O **membro nCmdShow** da estrutura *lpWindow* contém parâmetros para definir o estado da janela. Esse sinalizador é equivalente a chamar [ShowWindow](/windows/win32/api/winuser/nf-winuser-showwindow) com o *parâmetro state.* As constantes são as mesmas definidas no WINDOWS. H (como SW \_ HIDE, SW \_ MINIMIZE ou SW \_ SHOWNORMAL).

</dd> <dt>

<span id="MCI_OVLY_WINDOW_TEXT"></span><span id="mci_ovly_window_text"></span>TEXTO DA \_ JANELA MCI OVLY \_ \_
</dt> <dd>

O **membro lpstrText** da estrutura identificada por *lpWindow* contém um endereço de um buffer que contém a legenda usada para a janela.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, *o parâmetro lpWindow* aponta para uma estrutura [**MCI \_ OVLY \_ WINDOW \_ PARMS.**](mci-ovly-window-parms.md)

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

 

