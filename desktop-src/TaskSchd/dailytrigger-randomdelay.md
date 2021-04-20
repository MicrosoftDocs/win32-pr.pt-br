---
title: Propriedade DailyTrigger. RandomDelay
description: Para scripts, Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Propriedade DailyTrigger. RandomDelay
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Agendador de Tarefas da propriedade RandomDelay
- Propriedade RandomDelay Agendador de Tarefas, objeto DailyTrigger
- Objeto DailyTrigger Agendador de Tarefas, Propriedade RandomDelay
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303192d578a2681e250784c1e1eb2831c98482cc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734101"
---
# <a name="dailytriggerrandomdelay-property"></a>Propriedade DailyTrigger. RandomDelay

Para scripts, Obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.

## <a name="syntax"></a>Sintaxe


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valor da propriedade

O tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, P2DT5S é um atraso de 2 dias, 5 segundos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





