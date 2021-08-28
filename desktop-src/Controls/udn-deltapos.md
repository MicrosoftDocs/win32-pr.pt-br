---
title: UDN_DELTAPOS de notificação (Commctrl.h)
description: Enviado pelo sistema operacional para a janela pai de um controle para cima para baixo quando a posição do controle está prestes a mudar.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS código de notificação Windows Controles
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81285d2e0aa5c9a8b65eabf7c5b23d02da3acf02ac13e3274accce340530024f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088406"
---
# <a name="udn_deltapos-notification-code"></a>Código de notificação DELTAPOS da UDN \_

Enviado pelo sistema operacional para a janela pai de um controle para cima para baixo quando a posição do controle está prestes a mudar. Isso acontece quando o usuário solicita uma alteração no valor pressionando a seta para cima ou para baixo do controle. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) que contém informações sobre a alteração de posição. O **membro iPos** dessa estrutura contém a posição atual do controle. O **membro iDelta** da estrutura é um inteiro com sinal que contém a alteração proposta na posição. Se o usuário clicou no botão para cima, esse é um valor positivo. Se o usuário tiver clicado no botão para baixo, esse será um valor negativo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne a zero para impedir a alteração na posição do controle ou zero para permitir a alteração.

## <a name="remarks"></a>Comentários

O código de notificação DELTAPOS da UDN é enviado antes da mensagem \_ [**WM \_ VSCROLL**](wm-vscroll.md) ou [**WM \_ HSCROLL,**](wm-hscroll.md) que, na verdade, altera a posição do controle. Isso permite examinar, permitir, modificar ou não permitir a alteração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

