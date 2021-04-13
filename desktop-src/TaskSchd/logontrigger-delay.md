---
title: Propriedade LogonTrigger. Delay
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o usuário faz logon e quando a tarefa é iniciada.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto LogonTrigger
- Agendador de Tarefas de objeto LogonTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369341"
---
# <a name="logontriggerdelay-property"></a>Propriedade LogonTrigger. Delay

Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o usuário faz logon e quando a tarefa é iniciada.

## <a name="syntax"></a>Syntax


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a>Valor da propriedade

Um valor que indica a quantidade de tempo entre o momento em que o usuário faz logon e quando a tarefa é iniciada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o atraso do gatilho de logon é especificado usando o elemento [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





