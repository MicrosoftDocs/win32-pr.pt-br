---
title: Propriedade DailyTrigger.RandomDelay
description: Para scripts, obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. | Propriedade DailyTrigger.RandomDelay
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Propriedade RandomDelay Agendador de Tarefas
- Propriedade RandomDelay Agendador de Tarefas objeto , DailyTrigger
- Objeto DailyTrigger Agendador de Tarefas propriedade , RandomDelay
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
ms.openlocfilehash: bbc3bfec997b50a1f9d802191387a2186576532ca027e1086fc311b31f0da5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139469"
---
# <a name="dailytriggerrandomdelay-property"></a>Propriedade DailyTrigger.RandomDelay

Para scripts, obtém ou define um tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho.

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valor da propriedade

O tempo de atraso que é adicionado aleatoriamente à hora de início do gatilho. O formato dessa cadeia de caracteres `P<days>DT<hours>H<minutes>M<seconds>S` é (por exemplo, P2DT5S é um atraso de 2 dias e 5 segundos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DailyTrigger**](dailytrigger.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





