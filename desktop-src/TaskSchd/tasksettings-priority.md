---
title: Propriedade TaskSettings. Priority
description: Para scripts, Obtém ou define o nível de prioridade da tarefa.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Agendador de Tarefas da propriedade Priority
- Propriedade Priority Agendador de Tarefas, objeto TaskSettings
- Agendador de Tarefas de objeto TaskSettings, Propriedade Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b24c0281e8df314b070e0569176899b96071e1ef43caab17af4978e74f6b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354823"
---
# <a name="tasksettingspriority-property"></a>Propriedade TaskSettings. Priority

Para scripts, Obtém ou define o nível de prioridade da tarefa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>Valor da propriedade

O nível de prioridade (0-10) da tarefa. O padrão é 7.

## <a name="remarks"></a>Comentários

O nível de prioridade 0 é a prioridade mais alta, e o nível de prioridade 10 é a prioridade mais baixa. O valor padrão é 7. Os níveis de prioridade 7 e 8 são usados para tarefas em segundo plano, e os níveis de prioridade 4, 5 e 6 são usados para tarefas interativas.

A ação da tarefa é iniciada em um processo com uma prioridade baseada em um valor de classe de prioridade. Um valor de nível de prioridade (prioridade de thread) é usado para o manipulador COM, a caixa de mensagem e as ações de tarefa de email. Para obter mais informações sobre a classe de prioridade e os valores de nível de prioridade, consulte [prioridades de agendamento](/windows/desktop/ProcThread/scheduling-priorities). A tabela a seguir lista os valores possíveis para o parâmetro *Priority* e os valores de classe de prioridade e nível de prioridade correspondentes.



| *Prioridade* da tarefa | Classe de prioridade                 | Nível de prioridade                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | \_classe de prioridade em tempo real \_      | tempo de prioridade de THREAD \_ \_ \_ crítico |
| 1               | \_classe de prioridade alta \_          | prioridade de THREAD \_ \_ mais alta        |
| 2               | ACIMA \_ da \_ classe de prioridade normal \_ | prioridade de THREAD \_ \_ acima do \_ normal  |
| 3               | ACIMA \_ da \_ classe de prioridade normal \_ | prioridade de THREAD \_ \_ acima do \_ normal  |
| 4               | \_classe de prioridade normal \_        | prioridade de THREAD \_ \_ normal         |
| 5               | \_classe de prioridade normal \_        | prioridade de THREAD \_ \_ normal         |
| 6               | \_classe de prioridade normal \_        | prioridade de THREAD \_ \_ normal         |
| 7               | ABAIXO \_ da \_ classe de prioridade normal \_ | prioridade de THREAD \_ \_ abaixo do \_ normal  |
| 8               | ABAIXO \_ da \_ classe de prioridade normal \_ | prioridade de THREAD \_ \_ abaixo do \_ normal  |
| 9               | \_classe de prioridade ociosa \_          | \_prioridade \_ mais baixa da thread         |
| 10              | \_classe de prioridade ociosa \_          | prioridade de THREAD \_ \_ ociosa           |



 

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Priority (settingstype)**](taskschedulerschema-priority-settingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

