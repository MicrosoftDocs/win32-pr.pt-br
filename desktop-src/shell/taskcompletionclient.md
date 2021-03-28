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
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171172"
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

Essa API foi preterida e pode não estar disponível em versões futuras do Windows. Os aplicativos devem usar as APIs no namespace [**Windows. ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) em vez disso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
