---
title: Objeto RegistrationInfo
description: Objeto de script que fornece as informações administrativas que podem ser usadas para descrever a tarefa.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- informações de registro Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, descrito
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009098"
---
# <a name="registrationinfo-object"></a>Objeto RegistrationInfo

Objeto de script que fornece as informações administrativas que podem ser usadas para descrever a tarefa. Essas informações incluem detalhes como uma descrição da tarefa, o autor da tarefa, a data em que a tarefa é registrada e o descritor de segurança da tarefa.

## <a name="members"></a>Membros

O objeto **RegistrationInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **RegistrationInfo** tem essas propriedades.



| Propriedade                                                                     | Tipo de acesso           | Descrição                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autor**](registrationinfo-author.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define o autor da tarefa.<br/>                                                                                            |
| [**Date**](registrationinfo-date.md)<br/>                             | Leitura/gravação<br/> | Obtém ou define a data e a hora em que a tarefa é registrada.<br/>                                                                     |
| [**Descrição**](registrationinfo-description.md)<br/>               | Leitura/gravação<br/> | Obtém ou define a descrição da tarefa.<br/>                                                                                       |
| [**Documentação**](registrationinfo-documentation.md)<br/>           | Leitura/gravação<br/> | Obtém ou define qualquer documentação adicional para a tarefa.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Obtém ou define o descritor de segurança da tarefa.<br/>                                                                               |
| [**Original**](registrationinfo-source.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define de onde a tarefa foi originada. Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.<br/> |
| [**URI**](registrationinfo-uri.md)<br/>                               | Leitura/gravação<br/> | Obtém ou define o URI da tarefa.<br/>                                                                                               |
| [**Versão**](registrationinfo-version.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define o número de versão da tarefa.<br/>                                                                                    |
| [**XmlText**](registrationinfo-xmltext.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define uma versão formatada em XML das informações de registro da tarefa.<br/>                                             |



 

## <a name="remarks"></a>Comentários

As informações de registro podem ser usadas para identificar uma tarefa por meio da interface do usuário do Agendador de Tarefas ou como critérios de pesquisa ao enumerar as tarefas registradas.

Ao ler ou gravar XML para uma tarefa, as informações de registro para a tarefa são especificadas no elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





