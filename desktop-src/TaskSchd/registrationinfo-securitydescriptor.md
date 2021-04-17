---
title: Propriedade RegistrationInfo. SecurityDescriptor
description: Para scripts, Obtém ou define o descritor de segurança da tarefa.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Agendador de Tarefas da propriedade SecurityDescriptor
- Propriedade SecurityDescriptor Agendador de Tarefas, objeto RegistrationInfo
- Objeto RegistrationInfo Agendador de Tarefas, Propriedade SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782891"
---
# <a name="registrationinfosecuritydescriptor-property"></a>Propriedade RegistrationInfo. SecurityDescriptor

Para scripts, Obtém ou define o descritor de segurança da tarefa. Se um descritor de segurança diferente for fornecido durante o registro da tarefa, ele substituirá o descritor de segurança definido por essa propriedade.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Valor da propriedade

O descritor de segurança associado à tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o descritor de segurança da tarefa é especificado usando o elemento [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) do esquema de Agendador de tarefas.

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
</dt> </dl>

 

 





