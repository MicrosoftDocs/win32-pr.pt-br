---
title: Propriedade TaskSettings.RestartInterval
description: Para scripts, obtém ou define um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Propriedade RestartInterval Agendador de Tarefas
- A propriedade RestartInterval Agendador de Tarefas objeto , TaskSettings
- Objeto TaskSettings Agendador de Tarefas propriedade , RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293072fcec50b140a298887b12ed8f5dd1fb6a298c3b486069fe2e7eccaef00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681606"
---
# <a name="tasksettingsrestartinterval-property"></a>Propriedade TaskSettings.RestartInterval

Para scripts, obtém ou define um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valor da propriedade

Um valor que especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa. Se essa propriedade estiver definida, a [**propriedade RestartCount**](tasksettings-restartcount.md) também deverá ser definida. O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, "PT5M" é 5 minutos, "PT1H" é 1 hora e "PT20M" é 20 minutos). O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no [**elemento Interval**](taskschedulerschema-interval-restarttype-element.md) do esquema Agendador de Tarefas dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





