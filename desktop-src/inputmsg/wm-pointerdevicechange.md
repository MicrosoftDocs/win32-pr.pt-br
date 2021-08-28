---
title: WM_POINTERDEVICECHANGE mensagem
description: Enviado para uma janela quando há uma alteração nas configurações de um monitor que tem um digitalizador anexado a ela. Esta mensagem contém informações sobre o dimensionamento do modo de exibição.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- WM_POINTERDEVICECHANGE mensagens de entrada e notificações
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
ms.openlocfilehash: 6d75a5afa245303952c5c6b1814b2f1ce77cd03da7c789d34bda2500c6bffee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829576"
---
# <a name="wm_pointerdevicechange-message"></a>WM_POINTERDEVICECHANGE mensagem

Enviado para uma janela quando há uma alteração nas configurações de um monitor que tem um digitalizador anexado a ela. Esta mensagem contém informações sobre o dimensionamento do modo de exibição.

> \[! Importante\]  
> Os aplicativos da área de trabalho devem estar cientes de DPI. Se o aplicativo não estiver ciente de DPI, as coordenadas de tela contidas em mensagens de ponteiro e estruturas relacionadas poderão aparecer imprecisas devido à virtualização de DPI. A virtualização de DPI oferece suporte de dimensionamento automático para aplicativos que não têm conhecimento de DPI e estão ativos por padrão (os usuários podem desativar). Para obter mais informações, consulte [Escrevendo aplicativos Win32 de alto DPI.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contém um valor de [**Constantes de Alteração de Dispositivo de Ponteiro**](pointer-device-change-constants.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Obter informações adicionais específicas de mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o aplicativo processa essa mensagem, ele deve retornar zero.

Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens](messages.md)
</dt> </dl>

 

