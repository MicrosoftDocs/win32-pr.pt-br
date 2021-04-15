---
title: NM_CUSTOMDRAW código de notificação (commctrl. h)
description: Notifica uma janela pai do controle sobre as operações de desenho personalizadas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW de código de notificação controles do Windows
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454626"
---
# <a name="nm_customdraw-notification-code"></a>\_Código de notificação nm CUSTOMDRAW

Notifica uma janela pai do controle sobre as operações de desenho personalizadas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura relacionada ao empate personalizada que contém informações sobre a operação de desenho. A lista a seguir especifica os controles e suas estruturas associadas.



| Control                     | Estrutura de desenho Personalizada                    |
|-----------------------------|------------------------------------------|
| Rebar, TrackBar e header | [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| Modo de exibição de lista                   | [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| Dica de ferramenta                     | [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| Exibição em árvore                   | [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| Barra de ferramentas                     | [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor que seu aplicativo pode retornar depende do estágio de desenho atual. O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho. Você deve retornar um dos valores a seguir.



| Código de retorno                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**dopadrão CDRF \_**</dt> </dl>         | O controle será desenhado em si mesmo. Ele não enviará códigos de notificação [ \_ CUSTOMDRAW de nm](nm-customdraw.md) adicionais para este ciclo de pintura. Esse sinalizador não pode ser usado com nenhum outro sinalizador. <br/>                                                                                                                                                                                                                                 |
| <dl> <dt>**doborracha CDRF \_**</dt> </dl>           | O controle só desenhará o plano de fundo.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | Seu aplicativo especificou uma nova fonte para o item; o controle usará a nova fonte. Para obter mais informações sobre como alterar fontes, consulte [alterando fontes e cores](custom-draw.md). Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | O controle notificará o pai de qualquer operação de desenho relacionada a itens. Ele enviará códigos de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) antes e depois de itens de desenho. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | O controle notificará o pai depois de apagar um item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | O controle enviará um código de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) quando o ciclo de pintura de todo o controle for concluído. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ PrePaint.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | Seu aplicativo receberá um código de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) com **dwDrawStage** definido como CDDs \_ ITEMPREPAINT \| CDDs \_ subitem antes de cada subitem de exibição de lista ser desenhado. Em seguida, você pode especificar a fonte e a cor de cada subitem separadamente ou retornar [**CDRF \_ DODEFAULT**](cdrf-constants.md) para processamento padrão. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | Seu aplicativo desenhou o item manualmente. O controle não vai desenhar o item. Isso ocorre quando **dwDrawStage** é igual a CDDs \_ ITEMPREPAINT.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | O controle não desenhará o retângulo de foco em um item.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Comentários

Atualmente, os seguintes controles dão suporte à funcionalidade de desenho Personalizada: cabeçalho, exibição de lista, Rebar, barra de ferramentas, dica de ferramenta, TrackBar e modo de exibição de árvore. O desenho personalizado também terá suporte para controles de botão se você tiver um manifesto de aplicativo para garantir que Comctl32.dll versão 6 esteja disponível.

Se essa mensagem for tratada em um procedimento de caixa de diálogo, você deverá definir o valor de retorno como parte dos dados da janela antes de retornar **true**. Para obter mais informações, consulte [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Conceitua**
</dt> <dt>

[Desenho personalizado](custom-draw.md)
</dt> </dl>

 

