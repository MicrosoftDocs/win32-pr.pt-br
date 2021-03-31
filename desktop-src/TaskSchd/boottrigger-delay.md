---
title: Propriedade BootTrigger. Delay
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Agendador de Tarefas de propriedade de atraso
- Propriedade Delay Agendador de Tarefas, objeto BootTrigger
- Agendador de Tarefas de objeto BootTrigger, Propriedade Delay
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085885"
---
# <a name="boottriggerdelay-property"></a>Propriedade BootTrigger. Delay

Para scripts, Obtém ou define um valor que indica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada.

## <a name="syntax"></a>Sintaxe


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a>Valor da propriedade

Um valor que indica a quantidade de tempo entre o momento em que o sistema é inicializado e quando a tarefa é iniciada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="remarks"></a>Comentários

Ao ler ou gravar seu próprio XML para uma tarefa, o atraso de inicialização é especificado usando o elemento [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) do esquema de Agendador de tarefas.

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
</dt> <dt>

[**BootTrigger**](boottrigger.md)
</dt> </dl>

 

 





