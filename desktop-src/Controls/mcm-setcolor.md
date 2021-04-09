---
title: Mensagem de MCM_SETCOLOR (commctrl. h)
description: Define a cor de uma determinada parte de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a \_ macro setColor calendário mensal.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- Controles de MCM_SETCOLOR de mensagens do Windows
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
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086325"
---
# <a name="mcm_setcolor-message"></a>MCM \_ mensagem SETcolor

Define a cor de uma determinada parte de um controle de calendário mensal. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setColor calendário mensal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor do tipo **int** especificando qual cor de calendário de mês definir. Este valor pode ser um dos seguintes:



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

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor que será definida para a área especificada do calendário mensal.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a configuração de cor anterior para a parte especificada do controle de calendário mensal se for bem-sucedida. Caso contrário, o retorno será-1.

## <a name="remarks"></a>Comentários

Se os estilos visuais estiverem ativos, essa mensagem não terá efeito, exceto quando *wParam* for MCSC \_ background.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

