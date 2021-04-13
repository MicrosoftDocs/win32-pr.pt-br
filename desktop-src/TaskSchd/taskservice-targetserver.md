---
title: Propriedade TaskService. TargetServer
description: Para scripts, obtém o nome do computador que está executando o serviço de Agendador de Tarefas ao qual o usuário está conectado.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Agendador de Tarefas da Propriedade TargetServer
- Propriedade TargetServer Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, Propriedade TargetServer
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
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499810"
---
# <a name="taskservicetargetserver-property"></a>Propriedade TaskService. TargetServer

Para scripts, obtém o nome do computador que está executando o serviço de Agendador de Tarefas ao qual o usuário está conectado.

## <a name="syntax"></a>Syntax


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Valor da propriedade

O nome do computador que está executando o serviço de Agendador de Tarefas ao qual o usuário está conectado.

## <a name="remarks"></a>Comentários

Essa propriedade retorna uma cadeia de caracteres vazia quando o usuário passa um endereço IP, localhost ou '. ' como um parâmetro e retorna o nome do computador que está executando o serviço de Agendador de Tarefas quando o usuário não passa nenhum valor de parâmetro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





