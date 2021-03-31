---
title: Mensagem de DTM_GETSYSTEMTIME (commctrl. h)
description: Obtém a hora atualmente selecionada de um controle de data e hora (DTP) e o coloca em uma estrutura SYSTEMTIME especificada. Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime GetSystemTime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- Controles de DTM_GETSYSTEMTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085943"
---
# <a name="dtm_getsystemtime-message"></a>DTM \_ mensagem GETsystemtime

Obtém a hora atualmente selecionada de um controle de data e hora (DTP) e o coloca em uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) . Se **DTM \_ GetSystemTime** retornar \_ a GDT válida, essa estrutura conterá a hora atualmente selecionada. Caso contrário, ele não conterá informações válidas. Esse parâmetro deve ser um ponteiro válido; Não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna \_ a GDT válida se as informações de tempo foram colocadas com êxito em *lParam*. Retorna GDT \_ None se o controle foi definido como o estilo [**DTS não \_ None**](date-and-time-picker-control-styles.md) e a caixa de seleção controle não foi selecionada. Retorna \_ o erro da GDT se ocorrer um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

