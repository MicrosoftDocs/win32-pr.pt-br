---
title: Propriedade RegistrationInfo. Version
description: Para scripts, Obtém ou define o número de versão da tarefa.
ms.assetid: 5f200948-b4ff-495c-9578-2a93b34fd75b
keywords:
- Agendador de Tarefas de propriedade de versão
- Propriedade de versão Agendador de Tarefas, objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, Propriedade Version
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
ms.openlocfilehash: 4c312878383c5361317a765cbf84a503244c188a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009044"
---
# <a name="registrationinfoversion-property"></a>Propriedade RegistrationInfo. Version

Para scripts, Obtém ou define o número de versão da tarefa.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Version As String
```



## <a name="property-value"></a>Valor da propriedade

O número de versão da tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o número de versão da tarefa é especificado usando o elemento [**version**](taskschedulerschema-version-registrationinfotype-element.md) do esquema de Agendador de tarefas.

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

 

 





