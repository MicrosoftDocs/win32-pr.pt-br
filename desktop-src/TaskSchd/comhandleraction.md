---
title: Objeto ComHandlerAction
description: Objeto de script que representa uma ação que dispara um manipulador.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Ação do manipulador COM Agendador de Tarefas , objeto
- Objeto ComHandlerAction Agendador de Tarefas
- Objeto ComHandlerAction Agendador de Tarefas , descrito
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd803d67d292df22e651e4393880038835c862e0e81dde19e0d0a7e15fccd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659676"
---
# <a name="comhandleraction-object"></a>Objeto ComHandlerAction

Objeto de script que representa uma ação que dispara um manipulador.

## <a name="members"></a>Membros

O **objeto ComHandlerAction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto ComHandlerAction** tem essas propriedades.



| Propriedade                                               | Tipo de acesso           | Descrição                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Classid**](comhandleraction-classid.md)<br/> | Leitura/gravação<br/> | Obtém ou define o identificador da classe do manipulador.<br/>                                              |
| [**Dados**](comhandleraction-data.md)<br/>       | Leitura/gravação<br/> | Obtém ou define dados adicionais associados ao manipulador.<br/>                              |
| [**Id**](action-id.md)<br/>                     | Leitura/gravação<br/> | Herdado do [**objeto Action.**](action.md) Obtém ou define o identificador da ação.<br/> |
| [**Tipo**](action-type.md)<br/>                 | Somente leitura<br/>  | Herdado do [**objeto Action.**](action.md) Obtém o tipo da ação.<br/>               |



 

## <a name="remarks"></a>Comentários

Os manipuladores COM devem implementar a interface [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) para o Agendador de Tarefas iniciar e parar o manipulador. Por sua vez, o manipulador COM usa os métodos do objeto [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) para comunicar o status de volta ao Agendador de Tarefas.

Ao ler ou escrever XML, uma ação de manipulador COM é especificada no elemento [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) do Agendador de Tarefas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Agendador de Tarefas objetos](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





