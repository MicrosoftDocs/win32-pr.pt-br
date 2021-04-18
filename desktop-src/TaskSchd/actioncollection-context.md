---
title: Propriedade ActionCollection. Context
description: Para scripts, Obtém ou define o identificador da entidade de segurança da tarefa.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Agendador de Tarefas de propriedade de contexto
- Propriedade de contexto Agendador de Tarefas, objeto ActionCollection
- Agendador de Tarefas de objeto ActionCollection, Propriedade Context
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779893"
---
# <a name="actioncollectioncontext-property"></a>Propriedade ActionCollection. Context

Para scripts, Obtém ou define o identificador da entidade de segurança da tarefa.

## <a name="syntax"></a>Sintaxe


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a>Valor da propriedade

O identificador da entidade de segurança para a tarefa. O identificador especificado aqui deve corresponder ao identificador especificado na propriedade ID da interface IPrincipal que define a entidade de segurança.

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
</dt> <dt>

[**Açãocollection**](actioncollection.md)
</dt> </dl>

 

 





