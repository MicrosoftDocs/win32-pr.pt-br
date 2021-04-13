---
title: Objeto TaskDefinition
description: Objeto de script que define todos os componentes de uma tarefa, como as configurações de tarefa, os gatilhos, as ações e as informações de registro.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Agendador de Tarefas de objeto TaskDefinition
- Agendador de Tarefas de objeto TaskDefinition, descrito
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499474"
---
# <a name="taskdefinition-object"></a>Objeto TaskDefinition

Objeto de script que define todos os componentes de uma tarefa, como as configurações de tarefa, os gatilhos, as ações e as informações de registro.

## <a name="members"></a>Membros

O objeto **TaskDefinition** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **TaskDefinition** tem essas propriedades.



| Propriedade                                                               | Tipo de acesso           | Descrição                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ações**](taskdefinition-actions.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define uma coleção de ações que são executadas pela tarefa.<br/>                                                                                                         |
| [**Dados**](taskdefinition-data.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define os dados associados à tarefa. Esses dados são ignorados pelo serviço de Agendador de Tarefas, mas são usados por terceiros que desejam estender o formato de tarefa.<br/> |
| [**Beneficiário**](taskdefinition-principal.md)<br/>               | Leitura/gravação<br/> | Obtém ou define o principal para a tarefa que fornece as credenciais de segurança para a tarefa.<br/>                                                                                 |
| [**RegistrationInfo**](taskdefinition-registrationinfo.md)<br/> | Leitura/gravação<br/> | Obtém ou define as informações de registro que são usadas para descrever uma tarefa, como a descrição da tarefa, o autor da tarefa e a data em que a tarefa é registrada.<br/> |
| [**Configurações**](taskdefinition-settings.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define as configurações que definem como o serviço de Agendador de Tarefas executa a tarefa.<br/>                                                                                      |
| [**Gatilhos**](taskdefinition-triggers.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define uma coleção de gatilhos que são usados para iniciar uma tarefa.<br/>                                                                                                         |
| [**XmlText**](taskdefinition-xmltext.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define a definição formatada em XML da tarefa.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Ao ler ou gravar seu próprio XML para uma tarefa, uma definição de tarefa é especificada usando o elemento [**Task**](taskschedulerschema-task-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md) , [exemplo de gatilho de evento (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [exemplo de gatilho diário (script](daily-trigger-example--scripting-.md)), [exemplo de gatilho de registro (script)](registration-trigger-example--scripting-.md), exemplo de [gatilho semanal (Scripting)](weekly-trigger-example--scripting-.md), [exemplo de gatilho de logon (script)](logon-trigger-example--scripting-.md)ou [exemplo de gatilho de inicialização (script)](boot-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





