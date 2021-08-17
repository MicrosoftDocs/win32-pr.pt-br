---
title: Propriedade Principal.UserId
description: Para scripts, obtém ou define o identificador de usuário necessário para executar as tarefas associadas à entidade de entidade.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Propriedade UserId Agendador de Tarefas
- Propriedade UserId Agendador de Tarefas objeto , principal
- Objeto principal Agendador de Tarefas , propriedade UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9501184f3316e464aa26f42d51e0b4c27eccaeb72d447faa91edaa33b0b4774c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060024"
---
# <a name="principaluserid-property"></a>Propriedade Principal.UserId

Para scripts, obtém ou define o identificador de usuário necessário para executar as tarefas associadas à entidade de entidade.

## <a name="syntax"></a>Syntax


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Valor da propriedade

O identificador de usuário necessário para executar a tarefa.

## <a name="remarks"></a>Comentários

Não de definir essa propriedade se um identificador de grupo for especificado na [**propriedade GroupId.**](principal-groupid.md)

Ao ler ou escrever XML para uma tarefa, o identificador de usuário para a entidade de entidade é especificado usando o [**elemento UserId**](taskschedulerschema-userid-principaltype-element.md) do Agendador de Tarefas esquema.

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
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[**Principal.GroupId**](principal-groupid.md)
</dt> </dl>

 

 





