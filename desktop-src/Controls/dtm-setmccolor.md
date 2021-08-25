---
title: Mensagem de DTM_SETMCCOLOR (commctrl. h)
description: Define a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- controles de Windows de mensagem de DTM_SETMCCOLOR
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5154c2e450f5ef3c12c85fe3307f37958fea807226ab436241038c9ad639d4dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877816"
---
# <a name="dtm_setmccolor-message"></a>\_Mensagem DTM SETMCCOLOR

Define a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor do tipo **int** especificando qual cor de calendário de mês definir. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC \_ plano de fundo**</dt> </dl>       | Defina a cor do plano de fundo exibida entre meses.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Defina a cor do plano de fundo exibida no mês.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_texto MCSC**</dt> </dl>                         | Defina a cor usada para exibir o texto em um mês.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Defina a cor do plano de fundo exibida no título do calendário.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Defina a cor usada para exibir texto dentro do título do calendário.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Defina a cor usada para exibir o dia do cabeçalho e o texto do dia final. Os dias de cabeçalho e à direita são os dias dos meses anteriores e seguintes que aparecem no calendário do mês atual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor de **COLORREF** que representa a cor que será definida para a área especificada do calendário mensal.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **COLORREF** que representa a configuração de cor anterior para a parte especificada do controle de calendário mensal se for bem-sucedida. Caso contrário, a mensagem retornará-1.

## <a name="remarks"></a>Comentários

Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito, exceto quando *wParam* é MCSC \_ plano de fundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





