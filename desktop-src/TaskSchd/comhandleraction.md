---
title: Objeto comhandleaction
description: Objeto de script que representa uma ação que dispara um manipulador.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Ação do manipulador COM Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto comhandleaction
- Agendador de Tarefas de objeto comhandleaction, descrito
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
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454589"
---
# <a name="comhandleraction-object"></a>Objeto comhandleaction

Objeto de script que representa uma ação que dispara um manipulador.

## <a name="members"></a>Membros

O objeto **Comhandleaction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **Comhandleaction** tem essas propriedades.



| Propriedade                                               | Tipo de acesso           | Descrição                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**ClassId**](comhandleraction-classid.md)<br/> | Leitura/gravação<br/> | Obtém ou define o identificador da classe do manipulador.<br/>                                              |
| [**Dados**](comhandleraction-data.md)<br/>       | Leitura/gravação<br/> | Obtém ou define dados adicionais associados ao manipulador.<br/>                              |
| [**Sessão**](action-id.md)<br/>                     | Leitura/gravação<br/> | Herdado do objeto de [**ação**](action.md) . Obtém ou define o identificador da ação.<br/> |
| [**Tipo**](action-type.md)<br/>                 | Somente leitura<br/>  | Herdado do objeto de [**ação**](action.md) . Obtém o tipo da ação.<br/>               |



 

## <a name="remarks"></a>Comentários

Os manipuladores COM devem implementar a interface [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) para o Agendador de tarefas Iniciar e parar o manipulador. Por sua vez, o manipulador COM usa os métodos do objeto [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) para comunicar o status de volta para o Agendador de tarefas.

Ao ler ou gravar XML, uma ação de manipulador COM é especificada no elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Objetos Agendador de Tarefas](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





