---
title: Código de notificação do NM_CUSTOMDRAW (rebar) (commctrl. h)
description: Enviado pelo controle rebar para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- Windows controles de código de notificação NM_CUSTOMDRAW (rebar)
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 376bb9627d159dbb24080c2e475072dae357062975158d39f269e1cb7a4e3405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914866"
---
# <a name="nm_customdraw-rebar-notification-code"></a>\_Código de notificação do CUSTOMDRAW nm (rebar)

Enviado pelo controle rebar para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contém informações sobre a operação de desenho. O membro **dwItemSpec** dessa estrutura contém o identificador da banda que está sendo desenhada. O membro **lItemlParam** dessa estrutura contém o *lParam* da banda que está sendo desenhada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor que seu aplicativo pode retornar depende do estágio de desenho atual. O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho. Você deve retornar um dos valores a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**dopadrão CDRF \_**</dt> </dl>         | O controle será desenhado em si mesmo. Ele não enviará nenhuma notificação [de \_ CUSTOMDRAW nm](nm-customdraw.md) adicional para este ciclo de pintura. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | O controle notificará o pai de qualquer operação de desenho relacionada a itens. Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                           |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | O controle notificará o pai depois de apagar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | O controle notificará o pai depois de pintar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                               |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | O controle notificará o pai de qualquer operação de desenho relacionada a itens. Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                           |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | O aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte. Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md). Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | O aplicativo desenhou o item manualmente. O controle não vai desenhar o item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando o desenho personalizado](custom-draw.md)
</dt> </dl>

 

 





