---
title: Propriedade comhandleaction. Data
description: Para scripts, Obtém ou define dados adicionais associados ao manipulador.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Agendador de Tarefas de propriedade de dados
- Propriedade de dados Agendador de Tarefas, objeto comhandleaction
- Agendador de Tarefas de objeto comhandleaction, propriedade data
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
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369852"
---
# <a name="comhandleractiondata-property"></a>Propriedade comhandleaction. Data

Para scripts, Obtém ou define dados adicionais associados ao manipulador.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a>Valor da propriedade

Os argumentos que são necessários para o manipulador.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML, os dados de um manipulador COM são especificados no elemento [**Data**](taskschedulerschema-data-comhandlertype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Comhandleaction**](comhandleraction.md)
</dt> </dl>

 

 





