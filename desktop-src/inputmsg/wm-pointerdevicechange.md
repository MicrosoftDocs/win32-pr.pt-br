---
title: WM_POINTERDEVICECHANGE mensagem
description: Enviado a uma janela quando há uma alteração nas configurações de um monitor que tem um digitalizador anexado a ele. Esta mensagem contém informações sobre o dimensionamento do modo de exibição.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- Mensagens de entrada e notificações de WM_POINTERDEVICECHANGE mensagem
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794016"
---
# <a name="wm_pointerdevicechange-message"></a>WM_POINTERDEVICECHANGE mensagem

Enviado a uma janela quando há uma alteração nas configurações de um monitor que tem um digitalizador anexado a ele. Esta mensagem contém informações sobre o dimensionamento do modo de exibição.

> \[! Fundamental\]  
> Os aplicativos da área de trabalho devem ter reconhecimento de DPI. Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI. A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo). Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém um valor das [**constantes de alteração de dispositivo ponteiro**](pointer-device-change-constants.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Obter informações adicionais específicas de mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o aplicativo processar essa mensagem, ele deverá retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

