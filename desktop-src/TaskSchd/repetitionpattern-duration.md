---
title: Propriedade RepetitionPattern. Duration
description: Para scripts, Obtém ou define por quanto tempo o padrão é repetido.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Agendador de Tarefas da Propriedade Duration
- Propriedade Duration Agendador de Tarefas, objeto RepetitionPattern
- Agendador de Tarefas de objeto RepetitionPattern, Propriedade Duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758108"
---
# <a name="repetitionpatternduration-property"></a>Propriedade RepetitionPattern. Duration

Para scripts, Obtém ou define por quanto tempo o padrão é repetido.

## <a name="syntax"></a>Sintaxe


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a>Valor da propriedade

Por quanto tempo o padrão é repetido. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). O tempo mínimo permitido é de um minuto.

Se nenhum valor for especificado para a duração, o padrão será repetido indefinidamente.

## <a name="remarks"></a>Comentários

Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.

Ao ler ou gravar XML em uma tarefa, a duração da repetição é especificada no elemento [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





