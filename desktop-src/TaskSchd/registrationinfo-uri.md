---
title: Propriedade RegistrationInfo. URI
description: Para scripts, Obtém ou define o URI da tarefa.
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- Agendador de Tarefas de propriedade URI
- Propriedade URI Agendador de Tarefas, objeto RegistrationInfo
- Agendador de Tarefas de objeto RegistrationInfo, Propriedade URI
topic_type:
- apiref
api_name:
- RegistrationInfo.URI
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77598d556fdec29f41004529471c8098314a6faf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499613"
---
# <a name="registrationinfouri-property"></a>Propriedade RegistrationInfo. URI

Para scripts, Obtém ou define o URI da tarefa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>Valor da propriedade

O URI da tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o URI da tarefa é especificado usando o elemento [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





