---
title: Propriedade TaskSettings.Priority
description: Para scripts, obtém ou define o nível de prioridade da tarefa.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Propriedades de prioridade Agendador de Tarefas
- A propriedade Priority Agendador de Tarefas objeto , TaskSettings
- Objeto TaskSettings Agendador de Tarefas propriedade , Prioridade
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
# <a name="tasksettingspriority-property"></a>Propriedade TaskSettings.Priority

Para scripts, obtém ou define o nível de prioridade da tarefa.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>Valor da propriedade

O nível de prioridade (0 a 10) da tarefa. O padrão é 7.

## <a name="remarks"></a>Comentários

O nível de prioridade 0 é a prioridade mais alta e o nível de prioridade 10 é a prioridade mais baixa. O valor padrão é 7. Os níveis de prioridade 7 e 8 são usados para tarefas em segundo plano e os níveis de prioridade 4, 5 e 6 são usados para tarefas interativas.

A ação da tarefa é iniciada em um processo com uma prioridade baseada em um valor de Classe De Prioridade. Um valor de Nível de Prioridade (prioridade de thread) é usado para ações de tarefa de email, caixa de mensagem e manipulador COM. Para obter mais informações sobre os valores de Classe de Prioridade e Nível de Prioridade, consulte [Agendando prioridades](/windows/desktop/ProcThread/scheduling-priorities). A tabela a seguir lista os valores possíveis para o parâmetro *priority* e os valores de Priority Class e Priority Level correspondentes.



| Prioridade da *tarefa* | Classe Priority                 | Nível de prioridade                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | CLASSE \_ PRIORITY EM TEMPO \_ REAL      | TEMPO CRÍTICO \_ DE \_ PRIORIDADE DO \_ THREAD |
| 1               | CLASSE \_ DE ALTA \_ PRIORIDADE          | PRIORIDADE DE THREAD \_ \_ MAIS ALTA        |
| 2               | ACIMA \_ DA CLASSE DE PRIORIDADE \_ \_ NORMAL | PRIORIDADE \_ DE THREAD ACIMA DO \_ \_ NORMAL  |
| 3               | ACIMA \_ DA CLASSE DE PRIORIDADE \_ \_ NORMAL | PRIORIDADE \_ DE THREAD ACIMA DO \_ \_ NORMAL  |
| 4               | CLASSE \_ DE PRIORIDADE \_ NORMAL        | PRIORIDADE \_ DE \_ THREAD NORMAL         |
| 5               | CLASSE \_ DE PRIORIDADE \_ NORMAL        | PRIORIDADE \_ DE \_ THREAD NORMAL         |
| 6               | CLASSE \_ DE PRIORIDADE \_ NORMAL        | PRIORIDADE \_ DE \_ THREAD NORMAL         |
| 7               | ABAIXO \_ DA CLASSE DE PRIORIDADE \_ \_ NORMAL | PRIORIDADE \_ DO THREAD ABAIXO DO \_ \_ NORMAL  |
| 8               | ABAIXO \_ DA CLASSE DE PRIORIDADE \_ \_ NORMAL | PRIORIDADE \_ DO THREAD ABAIXO DO \_ \_ NORMAL  |
| 9               | CLASSE PRIORITY \_ \_ IDLE          | PRIORIDADE DE THREAD \_ \_ MAIS BAIXA         |
| 10              | CLASSE PRIORITY \_ \_ IDLE          | THREAD \_ PRIORITY \_ IDLE           |



 

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) do esquema Agendador de Tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

