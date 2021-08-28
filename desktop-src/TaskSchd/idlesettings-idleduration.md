---
title: Propriedade IdleSettings. IdleDuration
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes que a tarefa seja executada.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Agendador de Tarefas da propriedade IdleDuration
- Propriedade IdleDuration Agendador de Tarefas, objeto IdleSettings
- Objeto IdleSettings Agendador de Tarefas, Propriedade IdleDuration
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a78210202579d517410a2d82f1c5566d947f1ceb76cbd92538a0266b7b81ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002434"
---
# <a name="idlesettingsidleduration-property"></a>Propriedade IdleSettings. IdleDuration

Para scripts, Obtém ou define um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes que a tarefa seja executada.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a>Valor da propriedade

Um valor que indica a quantidade de tempo que o computador deve estar em um estado ocioso antes que a tarefa seja executada). O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). O valor mínimo é um minuto. Se esse valor for **nulo**, o atraso será definido como o padrão de 10 minutos.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





