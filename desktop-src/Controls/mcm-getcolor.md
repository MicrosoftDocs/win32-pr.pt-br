---
title: MCM_GETCOLOR mensagem (Commctrl.h)
description: Recupera a cor de uma determinada parte de um controle de calendário de mês. Você pode enviar essa mensagem explicitamente ou usando a \_ macro MonthCal GetColor.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- MCM_GETCOLOR controles de Windows mensagem
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254b140e801f4d4440c9b292999e5c8f91175a30750b08bfd30abd6afd84f73d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062086"
---
# <a name="mcm_getcolor-message"></a>Mensagem \_ GETCOLOR do MCM

Recupera a cor de uma determinada parte de um controle de calendário de mês. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ MonthCal GetColor.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do tipo **int que** especifica qual cor do calendário do mês recuperar. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**PLANO DE FUNDO DO \_ MCSC**</dt> </dl>       | Recupere a cor da tela de fundo exibida entre meses.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Recupere a cor da tela de fundo exibida dentro do mês.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**TEXTO \_ MCSC**</dt> </dl>                         | Recupere a cor usada para exibir o texto dentro de um mês.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Recupere a cor da tela de fundo exibida no título do calendário.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Recupere a cor usada para exibir o texto dentro do título do calendário.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Recupere a cor usada para exibir o dia do header e o texto do dia à frente. Os dias de início e à frente são os dias dos meses anteriores e a seguir que aparecem no calendário do mês atual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor COLORREF** que representa a configuração de cor para a parte especificada do controle de calendário do mês, se bem-sucedida. Caso contrário, essa mensagem retornará -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





