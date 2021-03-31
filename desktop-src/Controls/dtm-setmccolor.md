---
title: Mensagem de DTM_SETMCCOLOR (commctrl. h)
description: Define a cor de uma determinada parte do calendário mensal dentro de um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- Controles de DTM_SETMCCOLOR de mensagens do Windows
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
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644915"
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

## <a name="return-value"></a>Retornar valor

Retorna um valor **COLORREF** que representa a configuração de cor anterior para a parte especificada do controle de calendário mensal se for bem-sucedida. Caso contrário, a mensagem retornará-1.

## <a name="remarks"></a>Comentários

Quando os estilos visuais são habilitados, essa mensagem não tem nenhum efeito, exceto quando *wParam* é MCSC \_ plano de fundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





