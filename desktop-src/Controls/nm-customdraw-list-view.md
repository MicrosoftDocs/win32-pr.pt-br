---
title: Código de notificação de NM_CUSTOMDRAW (exibição de lista) (commctrl. h)
description: Enviado por um controle de exibição de lista para notificar suas janelas pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- NM_CUSTOMDRAW de código de notificação (exibição de lista) controles do Windows
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
ms.openlocfilehash: 19d8927006f3a6a7e5543f2b072d24469a73a7ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086540"
---
# <a name="nm_customdraw-list-view-notification-code"></a>\_Código de notificação nm CUSTOMDRAW (exibição de lista)

Enviado por um controle de exibição de lista para notificar suas janelas pai sobre operações de desenho. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) que contém informações sobre a operação de desenho. O primeiro membro dessa estrutura, **nmcd**, é um ponteiro para uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) . O membro **dwItemSpec** da estrutura apontada por **nmcd** contém o identificador do item que está sendo desenhado e o membro **lItemlParam** contém seus dados definidos pelo aplicativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor que seu aplicativo pode retornar depende do estágio de desenho atual. O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho. Você deve retornar um dos valores a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**dopadrão CDRF \_**</dt> </dl>         | O controle será desenhado em si mesmo. Ele não enviará nenhum código de notificação [ \_ CUSTOMDRAW de nm](nm-customdraw.md) adicional para este ciclo de pintura. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**doborracha CDRF \_**</dt> </dl>           | Windows Vista. O controle não desenhará o retângulo de foco em um item. <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | O controle notificará o pai de qualquer operação de desenho relacionada a itens. Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | O controle notificará o pai depois de apagar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | O controle notificará o pai depois de pintar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | O aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte. Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md). Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [Versão 4,71.](common-control-versions.md) Seu aplicativo receberá um código de controle [nm \_ CUSTOMDRAW](nm-customdraw.md) com **dwDrawStage** definido como CDDs \_ ITEMPREPAINT \| CDDs \_ subitem antes de cada subitem de exibição de lista ser desenhado. Em seguida, você pode especificar a fonte e a cor de cada subitem separadamente ou retornar [**CDRF \_ DODEFAULT**](cdrf-constants.md) para processamento padrão. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | O aplicativo desenhou o item manualmente. O controle não vai desenhar o item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | Windows Vista. O controle só pintará o plano de fundo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

[Versão 5,80.](common-control-versions.md) Se você alterar a fonte retornando [**CDRF \_ NEWFONT**](cdrf-constants.md), o controle de exibição de lista poderá exibir o texto recortado. Esse comportamento é necessário para compatibilidade com versões anteriores dos controles comuns. Se você quiser alterar a fonte de um controle de exibição de lista, obterá resultados melhores se enviar uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) com o valor *wParam* definido como 5 antes de adicionar qualquer item ao controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





