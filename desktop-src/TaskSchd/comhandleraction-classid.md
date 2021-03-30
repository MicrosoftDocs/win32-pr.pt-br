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
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644491"
---
# <a name="comhandleractionclassid-property"></a>Propriedade comhandleaction. ClassID

Para scripts, Obtém ou define o identificador da classe do manipulador.

## <a name="syntax"></a>Sintaxe


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Comhandleaction**](comhandleraction.md)
</dt> </dl>

 

 





