---
description: Habilita a conclusão da tarefa.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Interface TaskCompletionClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: d03e52a15e6689b7f1ea98a2f1021874cab6a8967dd148b7eaf685ff3984e8cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773646"
---
# <a name="taskcompletionclient-interface"></a>Interface TaskCompletionClient

Habilita a conclusão da tarefa.

## <a name="members"></a>Membros

A interface **TaskCompletionClient** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **TaskCompletionClient** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **TaskCompletionClient** tem esses métodos.



| Método                                                                    | Descrição                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**ApplyTaskCompletion**](taskcompletionclient-applytaskcompletion.md)   | Inicia a conclusão da tarefa.<br/> |
| [**RevokeTaskCompletion**](taskcompletionclient-revoketaskcompletion.md) | Encerra a conclusão da tarefa.<br/>   |



 

## <a name="remarks"></a>Comentários

O GUID desta interface é "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".

Essa API foi preterida e pode não estar disponível em versões futuras do Windows. Os aplicativos devem usar as APIs no [**Windows.**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041)Em vez disso, o namespace ApplicationModel. ExtendedExecution.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
