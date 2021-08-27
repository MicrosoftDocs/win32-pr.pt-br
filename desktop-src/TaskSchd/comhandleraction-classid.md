---
title: Propriedade comhandleaction. ClassID
description: Para scripts, Obtém ou define o identificador da classe do manipulador.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Agendador de Tarefas da propriedade ClassID
- Propriedade ClassID Agendador de Tarefas, objeto comhandleaction
- Objeto comhandleaction Agendador de Tarefas, Propriedade ClassID
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72338d4fe15936fcfe8f158098a798c4a3630cbd0587f46dc2f9346405477a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100456"
---
# <a name="comhandleractionclassid-property"></a>Propriedade comhandleaction. ClassID

Para scripts, Obtém ou define o identificador da classe do manipulador.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Valor da propriedade

O identificador da classe que define o manipulador a ser acionado.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML, a classe de um manipulador COM é especificada no elemento [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Comhandleaction**](comhandleraction.md)
</dt> </dl>

 

 





