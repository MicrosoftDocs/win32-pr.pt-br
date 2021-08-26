---
title: Propriedade RegistrationInfo. Source
description: Para scripts, Obtém ou define de onde a tarefa foi originada. Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.
ms.assetid: b5bd987f-5c9f-4af0-99e2-aec92951f2be
keywords:
- Agendador de Tarefas da propriedade de origem
- Propriedade Source Agendador de Tarefas, objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, Propriedade Source
topic_type:
- apiref
api_name:
- RegistrationInfo.Source
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97320d63823599e52327533afdba62f795622263e57878515ddd7ade9c98070b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126026"
---
# <a name="registrationinfosource-property"></a>Propriedade RegistrationInfo. Source

Para scripts, Obtém ou define de onde a tarefa foi originada. Por exemplo, uma tarefa pode se originar de um componente, serviço, aplicativo ou usuário.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Source As String
```



## <a name="property-value"></a>Valor da propriedade

De onde a tarefa foi originada. Por exemplo, de um componente, serviço, aplicativo ou usuário.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, as informações de origem da tarefa são especificadas usando o elemento [**Source**](taskschedulerschema-source-registrationinfotype-element.md) do esquema de Agendador de tarefas.

Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um recurso .dll arquivo. Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso. O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo de .dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso. Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





