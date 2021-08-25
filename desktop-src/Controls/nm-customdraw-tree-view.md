---
title: Código de notificação de NM_CUSTOMDRAW (exibição em árvore) (commctrl. h)
description: Enviado por um controle de exibição de árvore para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- código de notificação de NM_CUSTOMDRAW (exibição em árvore) Windows controles
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
ms.openlocfilehash: 9571d8461b43cebe047d80933af53a0c1aa1b865ede6280b8de2a33b74a60f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088836"
---
# <a name="nm_customdraw-tree-view-notification-code"></a>\_Código de notificação nm CUSTOMDRAW (exibição em árvore)

Enviado por um controle de exibição de árvore para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) que contém e recebe informações sobre a operação de desenho. O membro **dwItemSpec** do membro **nmcd** dessa estrutura contém o identificador do item que está sendo desenhado. O membro **lItemlParam** do membro **nmcd** dessa estrutura contém o *lParam* do item que está sendo desenhado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor que seu aplicativo pode retornar depende do estágio de desenho atual. O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho. Você deve retornar um dos valores a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**dopadrão CDRF \_**</dt> </dl>         | O controle se desenha. Ele não envia nenhum código [ \_ CUSTOMDRAW de nm](nm-customdraw.md) adicional para este ciclo de pintura. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | O controle notifica o pai de qualquer operação de desenho relacionada a itens. Ele envia códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | O controle notifica o pai depois de apagar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | O controle notifica o pai depois de pintar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versão 4,71.](common-control-versions.md) O controle notifica o pai quando um subitem de exibição de lista está sendo desenhado. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                  |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Seu aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte. Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md). Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Seu aplicativo desenhou o item manualmente. O controle não vai desenhar o item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

[Versão 5,80.](common-control-versions.md) Se você alterar a fonte retornando [**CDRF \_ NEWFONT**](cdrf-constants.md), o controle de exibição de árvore poderá exibir o texto recortado. Esse comportamento é necessário para compatibilidade com versões anteriores dos controles comuns. Se você quiser alterar a fonte de um controle de exibição de árvore, obterá resultados melhores se enviar uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) com o valor *wParam* definido como 5 antes de adicionar qualquer item ao controle.

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

 

 





