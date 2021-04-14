---
title: Propriedade Principal.Id
description: Para scripts, Obtém ou define o identificador da entidade de segurança.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Agendador de Tarefas de propriedade de ID
- Propriedade de ID Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369791"
---
# <a name="principalid-property"></a>Propriedade Principal.Id

Para scripts, Obtém ou define o identificador da entidade de segurança.

## <a name="syntax"></a>Syntax


```VB
Principal.Id As String
```



## <a name="property-value"></a>Valor da propriedade

O identificador da entidade de segurança.

## <a name="remarks"></a>Comentários

Esse identificador também é usado ao especificar a propriedade [**ActionCollection. Context**](actioncollection-context.md) .

Ao ler ou gravar XML para uma tarefa, o identificador da entidade de segurança é especificado no atributo ID do elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActionCollection. Context**](actioncollection-context.md)
</dt> <dt>

[**Beneficiário**](principal.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





