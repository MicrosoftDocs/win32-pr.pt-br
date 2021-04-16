---
title: Propriedade principal. GroupId
description: Para scripts, Obtém ou define o identificador do grupo de usuários que é necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Agendador de Tarefas da propriedade GroupId
- Propriedade GroupId Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779289"
---
# <a name="principalgroupid-property"></a>Propriedade principal. GroupId

Para scripts, Obtém ou define o identificador do grupo de usuários que é necessário para executar as tarefas associadas à entidade de segurança.

## <a name="syntax"></a>Sintaxe


```VB
Principal.GroupId As String
```



## <a name="property-value"></a>Valor da propriedade

O identificador do grupo de usuários que está associado a essa entidade de segurança.

## <a name="remarks"></a>Comentários

Não defina essa propriedade se um identificador de usuário for especificado na propriedade [**userid**](principal-userid.md) .

Ao ler ou gravar XML para uma tarefa, o identificador de grupo de uma entidade de segurança é especificado no elemento [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID**](principal-userid.md)
</dt> <dt>

[**Beneficiário**](principal.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





