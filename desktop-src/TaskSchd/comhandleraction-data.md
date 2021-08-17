---
title: Propriedade ComHandlerAction.Data
description: Para scripts, obtém ou define dados adicionais associados ao manipulador.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Dados de propriedade Agendador de Tarefas
- Propriedade de dados Agendador de Tarefas objeto , ComHandlerAction
- Objeto ComHandlerAction Agendador de Tarefas propriedade , Dados
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254457941d55d9a6b130ec504563236e60baf7ba1a1d44d5851ed3c712634afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139599"
---
# <a name="comhandleractiondata-property"></a>Propriedade ComHandlerAction.Data

Para scripts, obtém ou define dados adicionais associados ao manipulador.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a>Valor da propriedade

Os argumentos que são necessários para o manipulador.

## <a name="remarks"></a>Comentários

Ao ler ou escrever XML, os dados de um manipulador COM são especificados no elemento [**Data**](taskschedulerschema-data-comhandlertype-element.md) do esquema Agendador de Tarefas dados.

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

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





