---
title: Mensagem de DTM_SETMCFONT (commctrl. h)
description: Define a fonte a ser usada pelo controle de calendário do mês filho do controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- Controles de DTM_SETMCFONT de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455551"
---
# <a name="dtm_setmcfont-message"></a>\_Mensagem DTM SETMCFONT

Define a fonte a ser usada pelo controle de calendário do mês filho do controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a fonte que será definida.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica se o controle deve ser redesenhado imediatamente após a configuração da fonte. Definir esse parâmetro como **true** faz com que o controle seja redesenhado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





