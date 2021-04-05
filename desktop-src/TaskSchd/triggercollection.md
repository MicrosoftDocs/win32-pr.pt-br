---
title: Objeto TriggerCollection (Windows. UI. XAML. h)
description: Objeto de script que é usado para adicionar, remover e recuperar os gatilhos de uma tarefa.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- disparadores Agendador de Tarefas, objeto de coleção de gatilho
- Agendador de Tarefas de objeto TriggerCollection
- Agendador de Tarefas de objeto TriggerCollection, descrito
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085360"
---
# <a name="triggercollection-object"></a>Objeto TriggerCollection

Objeto de script que é usado para adicionar, remover e recuperar os gatilhos de uma tarefa.

## <a name="members"></a>Membros

O objeto **TriggerCollection** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **TriggerCollection** tem esses métodos.



| Método                                     | Descrição                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Formatação**](triggercollection-clear.md)   | Limpa todos os gatilhos da coleção.<br/>                                        |
| [**Criar**](triggercollection-create.md) | Cria um novo gatilho para a tarefa.<br/>                                             |
| [**Remover**](triggercollection-remove.md) | Remove o gatilho especificado da coleção de gatilhos usados pela tarefa.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **TriggerCollection** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Descrição                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Contar**](triggercollection-count.md)<br/> | Somente leitura<br/> | Obtém o número de gatilhos na coleção.<br/>  |
| [**Item**](triggercollection-item.md)<br/>   | Somente leitura<br/> | Obtém o gatilho especificado da coleção.<br/> |



 

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, os gatilhos para a tarefa são especificados no elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) do esquema de Agendador de tarefas.

Para obter informações sobre cada tipo de gatilho, consulte [tipos de gatilho](trigger-types.md).

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Windows. UI. XAML. h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Of**](trigger.md)
</dt> </dl>

 

 





