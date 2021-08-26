---
title: Objeto RegistrationInfo
description: Objeto de script que fornece as informações administrativas que podem ser usadas para descrever a tarefa.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- informações de registro Agendador de Tarefas , objeto
- Objeto RegistrationInfo Agendador de Tarefas
- Objeto RegistrationInfo Agendador de Tarefas , descrito
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
ms.openlocfilehash: f85bb423ae27a3d0b0b15f7b04d287a749f4fe23f3a4b58f7c2462b487b8a705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072646"
---
# <a name="registrationinfo-object"></a>Objeto RegistrationInfo

Objeto de script que fornece as informações administrativas que podem ser usadas para descrever a tarefa. Essas informações incluem detalhes como uma descrição da tarefa, o autor da tarefa, a data em que a tarefa é registrada e o descritor de segurança da tarefa.

## <a name="members"></a>Membros

O **objeto RegistrationInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto RegistrationInfo** tem essas propriedades.



| Propriedade                                                                     | Tipo de acesso           | Descrição                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autor**](registrationinfo-author.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define o autor da tarefa.<br/>                                                                                            |
| [**Data**](registrationinfo-date.md)<br/>                             | Leitura/gravação<br/> | Obtém ou define a data e a hora em que a tarefa é registrada.<br/>                                                                     |
| [**Descrição**](registrationinfo-description.md)<br/>               | Leitura/gravação<br/> | Obtém ou define a descrição da tarefa.<br/>                                                                                       |
| [**Documentação**](registrationinfo-documentation.md)<br/>           | Leitura/gravação<br/> | Obtém ou define qualquer documentação adicional para a tarefa.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Obtém ou define o descritor de segurança da tarefa.<br/>                                                                               |
| [**Fonte**](registrationinfo-source.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define de onde a tarefa foi originada. Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.<br/> |
| [**URI**](registrationinfo-uri.md)<br/>                               | Leitura/gravação<br/> | Obtém ou define o URI da tarefa.<br/>                                                                                               |
| [**Versão**](registrationinfo-version.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define o número de versão da tarefa.<br/>                                                                                    |
| [**Xmltext**](registrationinfo-xmltext.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define uma versão formatada em XML das informações de registro para a tarefa.<br/>                                             |



 

## <a name="remarks"></a>Comentários

As informações de registro podem ser usadas para identificar uma tarefa por meio da interface do usuário Agendador de Tarefas ou como critérios de pesquisa ao enumerar sobre as tarefas registradas.

Ao ler ou escrever XML para uma tarefa, as informações de registro da tarefa são especificadas no [**elemento RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) do esquema Agendador de Tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e um código de exemplo para esse objeto de script, consulte [Exemplo de gatilho de tempo (scripts).](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





