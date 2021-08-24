---
title: NM_CUSTOMDRAW (dica de ferramenta) de notificação (Commctrl.h)
description: Enviado por um controle de dica de ferramenta para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- NM_CUSTOMDRAW de notificação (dica de ferramenta) Windows Controles
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
ms.openlocfilehash: cc75a12bdf216c03892656f25dd41ba93c35346cf5aead08758f917fec29bb8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816376"
---
# <a name="nm_customdraw-tooltip-notification-code"></a>Código de \_ notificação NM CUSTOMDRAW (dica de ferramenta)

Enviado por um controle de dica de ferramenta para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) que contém informações sobre a operação de desenho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor que seu aplicativo pode retornar depende do estágio de desenho atual. O **membro dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica a fase de desenho. Você deve retornar um dos valores a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | O controle se desenhará. Ele não enviará nenhum código de [notificação \_ CUSTOMDRAW de NM](nm-customdraw.md) adicional para esse ciclo de pintura. Isso ocorre quando **dwDrawStage** é igual a CDDS \_ PREPAINT.<br/>                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | O controle notificará o pai de todas as operações de desenho relacionadas ao item. Ele enviará códigos [de \_ notificação CUSTOMDRAW de NM](nm-customdraw.md) antes e depois de desenhar itens. Isso ocorre quando **dwDrawStage** é igual a CDDS \_ PREPAINT.<br/>                                            |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | O controle notificará o pai depois de apagar um item. Isso ocorre quando **dwDrawStage** é igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | O controle notificará o pai depois de pintar um item. Isso ocorre quando **dwDrawStage** é igual a CDDS \_ PREPAINT.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versão 4.71.](common-control-versions.md) O controle notificará o pai quando um subitem de exibição de lista estiver sendo desenhado. Isso ocorre quando **dwDrawStage** é igual a CDDS \_ PREPAINT.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Seu aplicativo especificou uma nova fonte para o item. O controle usará a nova fonte. Para obter mais informações sobre como alterar fontes, consulte [Alterando fontes e cores](custom-draw.md). Isso ocorre quando **dwDrawStage** é igual a CDDS \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Seu aplicativo extraia o item manualmente. O controle não desenhará o item. Isso ocorre quando **dwDrawStage** é igual a CDDS \_ ITEMPREPAINT.<br/>                                                                                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando o desenho personalizado](custom-draw.md)
</dt> </dl>

 

 





