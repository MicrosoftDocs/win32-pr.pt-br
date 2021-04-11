---
title: Propriedade IdleSettings. WaitTimeout
description: Para scripts, Obtém ou define um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Agendador de Tarefas da propriedade WaitTimeout
- Propriedade WaitTimeout Agendador de Tarefas, objeto IdleSettings
- Objeto IdleSettings Agendador de Tarefas, Propriedade WaitTimeout
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009470"
---
# <a name="idlesettingswaittimeout-property"></a>Propriedade IdleSettings. WaitTimeout

Para scripts, Obtém ou define um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa. Se nenhum valor for especificado para essa propriedade, o serviço de Agendador de Tarefas aguardará indefinidamente se uma condição ociosa ocorrer.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a>Valor da propriedade

Um valor que indica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). O tempo mínimo permitido é de 1 minuto. Se esse valor for **nulo**, o atraso será definido como o padrão de 1 hora.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) do esquema de Agendador de tarefas.

Se uma tarefa for disparada por um gatilho ocioso, a propriedade **IdleSettings. WaitTimeout** será ignorada.

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

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





