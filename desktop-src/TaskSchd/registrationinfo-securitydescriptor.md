---
title: Propriedade RegistrationInfo.SecurityDescriptor
description: Para scripts, obtém ou define o descritor de segurança da tarefa.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Propriedade SecurityDescriptor Agendador de Tarefas
- Propriedade SecurityDescriptor Agendador de Tarefas objeto , RegistrationInfo
- Objeto RegistrationInfo Agendador de Tarefas , propriedade SecurityDescriptor
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
ms.openlocfilehash: c5c3aa83bc05952007d9114ad9812068de5b5b0bd82a4ce9e14e4d5ba1025bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759557"
---
# <a name="registrationinfosecuritydescriptor-property"></a>Propriedade RegistrationInfo.SecurityDescriptor

Para scripts, obtém ou define o descritor de segurança da tarefa. Se um descritor de segurança diferente for fornecido durante o registro da tarefa, ele será substituído pelo descritor de segurança definido com essa propriedade.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Valor da propriedade

O descritor de segurança associado à tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, o descritor de segurança da tarefa é especificado usando o elemento [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) do Agendador de Tarefas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





