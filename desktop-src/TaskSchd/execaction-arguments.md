---
title: Propriedade ExecAction.Arguments
description: Para scripts, obtém ou define os argumentos associados à operação de linha de comando.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Propriedades de argumentos Agendador de Tarefas
- Propriedade Arguments Agendador de Tarefas objeto , ExecAction
- Objeto ExecAction Agendador de Tarefas propriedade , Arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899e4ceaaf3a0d04dc678592add18184401d54569fea71f0570a0acbf2a33027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011486"
---
# <a name="execactionarguments-property"></a>Propriedade ExecAction.Arguments

Para scripts, obtém ou define os argumentos associados à operação de linha de comando.

## <a name="syntax"></a>Syntax


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Valor da propriedade

Os argumentos necessários para a operação de linha de comando.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML, os argumentos de operação de linha de comando são especificados no [**elemento Arguments**](taskschedulerschema-arguments-exectype-element.md) do Agendador de Tarefas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





