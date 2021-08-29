---
title: Propriedade TaskService.TargetServer
description: Para scripts, obtém o nome do computador que está executando o Agendador de Tarefas serviço ao que o usuário está conectado.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Propriedade TargetServer Agendador de Tarefas
- Propriedade TargetServer Agendador de Tarefas objeto , TaskService
- Objeto TaskService Agendador de Tarefas propriedade , TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79f68dfaf5d6000ad88dca9001102056eb349601630364105526ea0d29a8bf46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080286"
---
# <a name="taskservicetargetserver-property"></a>Propriedade TaskService.TargetServer

Para scripts, obtém o nome do computador que está executando o Agendador de Tarefas serviço ao que o usuário está conectado.

## <a name="syntax"></a>Syntax


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Valor da propriedade

O nome do computador que está executando o Agendador de Tarefas serviço ao que o usuário está conectado.

## <a name="remarks"></a>Comentários

Essa propriedade retorna uma cadeia de caracteres vazia quando o usuário passa um endereço IP, Localhost ou '.' como um parâmetro e retorna o nome do computador que está executando o serviço Agendador de Tarefas quando o usuário não passa nenhum valor de parâmetro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





