---
description: A seguir estão as constantes de movimentos.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Constantes de movimentos (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e927d0715c9f34e7e1db979c32545a0d8c8efad18186192a751f2cdbed13172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092643"
---
# <a name="flicks-constants"></a>Constantes de movimentos

A seguir estão as constantes de movimentos.



| Constante/valor                                                                                                                                                                                                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**Movimento \_ O WM \_ tratou a \_ máscara**</dt> <dt>0x1</dt> </dl> | O valor a ser retornado após a manipulação da mensagem de [**\_ mensagem de \_ movimento do WM Tablet**](wm-tablet-flick-message.md) . Se **a \_ \_ \_ máscara manipulada do WM em movimento** for retornada, nenhuma ação adicional ocorrerá. caso contrário, Windows envia notificações de acompanhamento, como o [**wm \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), o [**wm \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)ou o [**wm \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown), dependendo de qual ação está associada ao movimento da caneta. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**Número \_ de \_Direções de movimento**</dt> <dt>8</dt> </dl>       | O número de direções definidas na enumeração [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Tabflicks. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Enumeração FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**Mensagem de movimento do \_ Tablet do WM \_**](wm-tablet-flick-message.md)
</dt> <dt>

[Gestos de movimentos](flicks-gestures.md)
</dt> <dt>

[Respondendo a movimentos de caneta](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

