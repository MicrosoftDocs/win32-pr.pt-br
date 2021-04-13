---
title: Propriedade RegistrationTrigger. Delay
description: Para scripts, Obtém ou define a quantidade de tempo entre a qual a tarefa é registrada e quando a tarefa é iniciada.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto RegistrationTrigger
- Agendador de Tarefas de objeto RegistrationTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499649"
---
# <a name="registrationtriggerdelay-property"></a>Propriedade RegistrationTrigger. Delay

Para scripts, Obtém ou define a quantidade de tempo entre a qual a tarefa é registrada e quando a tarefa é iniciada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="syntax"></a>Syntax


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a>Valor da propriedade

A quantidade de tempo entre quando o sistema é registrado e quando a tarefa é iniciada.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o atraso de inicialização é especificado usando o elemento [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) do esquema de Agendador de tarefas.

Se uma tarefa com um gatilho de registro atrasado for registrada e o computador em que a tarefa está registrada for desligado ou reiniciado durante o atraso, antes da execução da tarefa, a tarefa não será executada e o atraso será perdido.

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

 

 





