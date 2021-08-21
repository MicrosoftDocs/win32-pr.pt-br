---
title: Propriedade TimeTrigger.RandomDelay
description: Para scripts, obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Propriedade TimeTrigger.RandomDelay
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Propriedade RandomDelay Agendador de Tarefas
- Propriedade RandomDelay Agendador de Tarefas objeto , TimeTrigger
- Objeto TimeTrigger Agendador de Tarefas propriedade , RandomDelay
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdbe297ace4fd34c2b5bf88db132e0573afd208052b50331ab571881b85831f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354758"
---
# <a name="timetriggerrandomdelay-property"></a>Propriedade TimeTrigger.RandomDelay

Para scripts, obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.

## <a name="syntax"></a>Syntax


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valor da propriedade

O tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, em que nY é o número de anos, nM é o número de meses, nD é o número de dias, 'T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





