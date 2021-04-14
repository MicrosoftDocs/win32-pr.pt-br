---
title: Código de notificação de NM_CUSTOMDRAW (barra de ferramentas) (commctrl. h)
description: Enviado por uma barra de ferramentas para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e83a85f4-7955-411d-9a08-29f5b30158c5
keywords:
- Código de notificação de NM_CUSTOMDRAW (barra de ferramentas) controles do Windows
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
ms.openlocfilehash: c8d1a33e6b7e9a26237813ec3a90e560f05dd9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499866"
---
# <a name="nm_customdraw-toolbar-notification-code"></a>\_Código de notificação nm CUSTOMDRAW (barra de ferramentas)

Enviado por uma barra de ferramentas para notificar sua janela pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW
        
    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versão 4,70](common-control-versions.md). Ponteiro para uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contém informações sobre a operação de desenho. O membro **dwItemSpec** dessa estrutura contém o identificador de comando do item que está sendo desenhado. O membro **lItemlParam** dessa estrutura contém o valor **dwData** para o item que está sendo desenhado.

[Versão 4,71](common-control-versions.md). Ponteiro para uma estrutura [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) que contém informações sobre a operação de desenho. O membro **dwItemSpec** do membro **nmcd** dessa estrutura contém o identificador de comando do item que está sendo desenhado. O membro **lItemlParam** do membro **nmcd** dessa estrutura contém o valor **dwData** para o item que está sendo desenhado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor que seu aplicativo pode retornar depende do estágio de desenho atual. O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho. Você deve retornar um dos valores a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**dopadrão CDRF \_**</dt> </dl>         | O controle será desenhado em si mesmo. Ele não enviará nenhum código de notificação [ \_ CUSTOMDRAW de nm](nm-customdraw.md) adicional para este ciclo de pintura. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | O controle notificará o pai de qualquer operação de desenho relacionada a itens. Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | O controle notificará o pai depois de apagar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | O controle notificará o pai depois de pintar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versão 4,71](common-control-versions.md). O controle notificará o pai quando um subitem de exibição de lista estiver sendo desenhado. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Seu aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte. Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md). Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Seu aplicativo desenhou o item manualmente. O controle não vai desenhar o item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                       |
| <dl> <dt>**TBCDRF \_ BLENDICON**</dt> </dl>       | [Versão 5, 0](common-control-versions.md). Misture o botão 50 por cento com o plano de fundo. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                      |
| <dl> <dt>**TBCDRF \_ NObackground**</dt> </dl>    | [Versão 5, 0](common-control-versions.md). Não desenhe o plano de fundo do botão. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**TBCDRF \_ NObordas**</dt> </dl>         | [Versão 4,71](common-control-versions.md). Não desenhe bordas de botão. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                             |
| <dl> <dt>**TBCDRF \_ HILITEHOTTRACK**</dt> </dl>  | [Versão 4,71](common-control-versions.md). Use o membro **clrHighlightHotTrack** da estrutura [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) para desenhar o plano de fundo de itens de rastreamento dinâmico. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                        |
| <dl> <dt>**TBCDRF \_ NOoffset**</dt> </dl>        | [Versão 4,71](common-control-versions.md). Não deslocar o botão quando pressionado. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                |
| <dl> <dt>**TBCDRF \_ NOmark**</dt> </dl>          | Não desenhe o realce padrão de itens que têm o [**TBSTATE \_ marcado**](toolbar-button-states.md). Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                              |
| <dl> <dt>**TBCDRF \_ NOETCHEDEFFECT**</dt> </dl>  | [Versão 4,71](common-control-versions.md). Não desenhe o efeito esboçado para itens desabilitados. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                         |
| <dl> <dt>**TBCDRF \_ USECDCOLORS**</dt> </dl>     | [Versão 6, 0](common-control-versions.md), somente **Windows Vista** . Use cores de desenho personalizadas para renderizar texto independentemente do estilo visual.<br/>                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando o desenho personalizado](custom-draw.md)
</dt> </dl>

 

 





