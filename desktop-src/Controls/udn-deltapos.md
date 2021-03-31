---
title: UDN_DELTAPOS código de notificação (commctrl. h)
description: Enviado pelo sistema operacional para a janela pai de um controle de cima para baixo quando a posição do controle está prestes a ser alterada.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS de código de notificação controles do Windows
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
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644695"
---
# <a name="udn_deltapos-notification-code"></a>Código de notificação do UDN \_ DELTAPOS

Enviado pelo sistema operacional para a janela pai de um controle de cima para baixo quando a posição do controle está prestes a ser alterada. Isso acontece quando o usuário solicita uma alteração no valor pressionando a seta para cima ou para baixo do controle. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) que contém informações sobre a alteração de posição. O membro **IPOs** dessa estrutura contém a posição atual do controle. O membro **Idelta** da estrutura é um inteiro assinado que contém a alteração proposta na posição. Se o usuário clicou no botão para cima, esse é um valor positivo. Se o usuário clicou no botão para baixo, esse é um valor negativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne diferente de zero para impedir a alteração na posição do controle ou zero para permitir a alteração.

## <a name="remarks"></a>Comentários

O \_ código de notificação UDN DELTAPOS é enviado antes da mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) ou do [**WM \_ HSCROLL**](wm-hscroll.md) , que, na verdade, altera a posição do controle. Isso permite que você examine, permita, modifique ou proíba a alteração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

