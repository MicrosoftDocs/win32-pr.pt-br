---
title: Objeto TriggerCollection (Windows.ui.xaml.h)
description: Objeto de script usado para adicionar, remover de e recuperar os gatilhos de uma tarefa.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- dispara Agendador de Tarefas , disparar objeto de coleção
- Objeto TriggerCollection Agendador de Tarefas
- Objeto TriggerCollection Agendador de Tarefas , descrito
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
ms.openlocfilehash: c7fd103918bc3898e56a3041221c9c70c9ede9aea5df4843cd984f2502279014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001934"
---
# <a name="triggercollection-object"></a>Objeto TriggerCollection

Objeto de script usado para adicionar, remover de e recuperar os gatilhos de uma tarefa.

## <a name="members"></a>Membros

O **objeto TriggerCollection** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto TriggerCollection** tem esses métodos.



| Método                                     | Descrição                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Limpar**](triggercollection-clear.md)   | Limpa todos os gatilhos da coleção.<br/>                                        |
| [**Criar**](triggercollection-create.md) | Cria um novo gatilho para a tarefa.<br/>                                             |
| [**Remover**](triggercollection-remove.md) | Remove o gatilho especificado da coleção de gatilhos usados pela tarefa.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto TriggerCollection** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Descrição                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Contagem**](triggercollection-count.md)<br/> | Somente leitura<br/> | Obtém o número de gatilhos na coleção.<br/>  |
| [**Item**](triggercollection-item.md)<br/>   | Somente leitura<br/> | Obtém o gatilho especificado da coleção.<br/> |



 

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, os gatilhos para a tarefa são especificados no elemento [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) do Agendador de Tarefas esquema.

Para obter informações sobre cada tipo de gatilho, consulte [Tipos de gatilho](trigger-types.md).

## <a name="examples"></a>Exemplos

Para obter mais informações e um código de exemplo para esse objeto de script, consulte [Exemplo de gatilho de tempo (scripts).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Windows.ui.xaml.h</dt> </dl> |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gatilho**](trigger.md)
</dt> </dl>

 

 





