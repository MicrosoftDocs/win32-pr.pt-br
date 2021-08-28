---
title: MCM_SETCOLOR mensagem (Commctrl.h)
description: Define a cor de uma determinada parte de um controle de calendário de mês. Você pode enviar essa mensagem explicitamente ou usando a macro MonthCal \_ SetColor.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- MCM_SETCOLOR controles Windows mensagem
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0915f78ad2dc666d6476cebb51be4f8b8c6102cb1433da59af7b9a1342deedc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697145"
---
# <a name="mcm_setcolor-message"></a>Mensagem MCM \_ SETCOLOR

Define a cor de uma determinada parte de um controle de calendário de mês. Você pode enviar essa mensagem explicitamente ou usando a macro [**MonthCal \_ SetColor.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do tipo **int que** especifica qual cor do calendário de mês deve ser definida. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**PLANO DE FUNDO DO \_ MCSC**</dt> </dl>       | Definir a cor da tela de fundo exibida entre meses.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | De definir a cor da tela de fundo exibida dentro do mês.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**TEXTO \_ MCSC**</dt> </dl>                         | Definir a cor usada para exibir o texto dentro de um mês.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Definir a cor da tela de fundo exibida no título do calendário.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Definir a cor usada para exibir o texto dentro do título do calendário.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Definir a cor usada para exibir o dia do header e o texto do dia à frente. Os dias de início e à frente são os dias dos meses anteriores e a seguir que aparecem no calendário do mês atual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**Valor COLORREF**](/windows/desktop/gdi/colorref) que representa a cor que será definida para a área especificada do calendário do mês.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um [**valor COLORREF**](/windows/desktop/gdi/colorref) que representa a configuração de cor anterior para a parte especificada do controle de calendário do mês, se bem-sucedida. Caso contrário, o retorno será -1.

## <a name="remarks"></a>Comentários

Se os estilos visuais estão ativos, essa mensagem não terá nenhum efeito, exceto quando *wParam* for MCSC \_ BACKGROUND.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

