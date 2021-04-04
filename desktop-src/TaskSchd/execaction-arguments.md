---
title: Propriedade execaction. Arguments
description: Para scripts, Obtém ou define os argumentos associados à operação de linha de comando.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Propriedade Arguments Agendador de Tarefas
- Propriedade Arguments Agendador de Tarefas, objeto Execaction
- Agendador de Tarefas de objeto execaction, Propriedade Arguments
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
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918218"
---
# <a name="execactionarguments-property"></a>Propriedade execaction. Arguments

Para scripts, Obtém ou define os argumentos associados à operação de linha de comando.

## <a name="syntax"></a>Syntax


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Valor da propriedade

Os argumentos que são necessários para a operação de linha de comando.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML, os argumentos da operação de linha de comando são especificados no elemento [**arguments**](taskschedulerschema-arguments-exectype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Execaction**](execaction.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





