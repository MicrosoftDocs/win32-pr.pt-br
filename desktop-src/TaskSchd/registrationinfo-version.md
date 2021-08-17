---
title: Propriedade RegistrationInfo.Version
description: Para scripts, obtém ou define o número de versão da tarefa.
ms.assetid: 5f200948-b4ff-495c-9578-2a93b34fd75b
keywords:
- Propriedade version Agendador de Tarefas
- Propriedade version Agendador de Tarefas objeto , RegistrationInfo
- Objeto RegistrationInfo Agendador de Tarefas , propriedade Version
topic_type:
- apiref
api_name:
- RegistrationInfo.Version
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08ef170004b7c9791f18cf65360c2446d5c87a6b835fb6fbcb048f47892c470
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059984"
---
# <a name="registrationinfoversion-property"></a>Propriedade RegistrationInfo.Version

Para scripts, obtém ou define o número de versão da tarefa.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Version As String
```



## <a name="property-value"></a>Valor da propriedade

O número de versão da tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, o número de versão da tarefa é especificado usando o elemento [**Version**](taskschedulerschema-version-registrationinfotype-element.md) do Agendador de Tarefas esquema.

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

 

 





