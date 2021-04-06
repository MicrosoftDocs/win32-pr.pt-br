---
title: Mensagem de MCM_GETCOLOR (commctrl. h)
description: Recupera a cor de uma determinada parte de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetColor calendário mensal.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- Controles de MCM_GETCOLOR de mensagens do Windows
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
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086148"
---
# <a name="mcm_getcolor-message"></a>MCM \_ mensagem GETcolor

Recupera a cor de uma determinada parte de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetColor calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do tipo **int** que especifica qual cor de calendário de mês deve ser recuperada. Este valor pode ser um dos seguintes:



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <dt>**MCSC \_ plano de fundo**</dt> </dl>       | Recupere a cor de plano de fundo exibida entre meses.<br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <dt>**MCSC \_ MONTHBK**</dt> </dl>                | Recupere a cor do plano de fundo exibida no mês.<br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <dt>**\_texto MCSC**</dt> </dl>                         | Recupere a cor usada para exibir o texto em um mês.<br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <dt>**MCSC \_ TITLEBK**</dt> </dl>                | Recupere a cor do plano de fundo exibida no título do calendário.<br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <dt>**MCSC \_ TITLETEXT**</dt> </dl>          | Recupere a cor usada para exibir texto dentro do título do calendário.<br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <dt>**MCSC \_ TRAILINGTEXT**</dt> </dl> | Recupere a cor usada para exibir o dia do cabeçalho e o texto do dia final. Os dias de cabeçalho e à direita são os dias dos meses anteriores e seguintes que aparecem no calendário do mês atual.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **COLORREF** que representa a configuração de cor para a parte especificada do controle de calendário mensal se tiver êxito. Caso contrário, essa mensagem retornará-1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





