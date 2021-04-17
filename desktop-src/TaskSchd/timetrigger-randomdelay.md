---
title: Propriedade timetrigger. RandomDelay
description: Para scripts, Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Propriedade timetrigger. RandomDelay
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Agendador de Tarefas da propriedade RandomDelay
- Agendador de Tarefas da propriedade RandomDelay, objeto timetrigger
- Agendador de Tarefas de objeto timetrigger, Propriedade RandomDelay
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
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105754718"
---
# <a name="timetriggerrandomdelay-property"></a>Propriedade timetrigger. RandomDelay

Para scripts, Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.

## <a name="syntax"></a>Syntax


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valor da propriedade

O tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





