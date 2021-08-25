---
title: Propriedade EventTrigger. Delay
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.
ms.assetid: 6f8b5e25-ad53-466e-adab-fe3c968e941b
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto EventTrigger
- Agendador de Tarefas de objeto EventTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- EventTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402ddb8e55f6eb22a4e2c106b64cbec3ed1afa6d0b58f38a2a8923f5bd8dfa4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959586"
---
# <a name="eventtriggerdelay-property"></a>Propriedade EventTrigger. Delay

Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="syntax"></a>Syntax


```VB
EventTrigger.Delay As String
```



## <a name="property-value"></a>Valor da propriedade

Um valor que indica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.

## <a name="remarks"></a>Comentários

Ao ler ou gravar seu próprio XML para uma tarefa, o atraso do evento é especificado usando o elemento [**Delay**](taskschedulerschema-delay-eventtriggertype-element.md) do esquema de Agendador de tarefas.

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

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

 





