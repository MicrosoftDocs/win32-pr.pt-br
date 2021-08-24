---
title: Propriedade RegistrationInfo.URI
description: Para scripts, obtém ou define o URI da tarefa.
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- Propriedades de URI Agendador de Tarefas
- Propriedade URI Agendador de Tarefas objeto , RegistrationInfo
- Objeto RegistrationInfo Agendador de Tarefas propriedade , URI
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
ms.openlocfilehash: 94c34c5dee30115ee430ad072d26e4bd67879988a9f2633cf9da9304e31324b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034076"
---
# <a name="registrationinfouri-property"></a>Propriedade RegistrationInfo.URI

Para scripts, obtém ou define o URI da tarefa.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>Valor da propriedade

O URI da tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML para uma tarefa, o URI da tarefa é especificado usando o elemento [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) do esquema Agendador de Tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





