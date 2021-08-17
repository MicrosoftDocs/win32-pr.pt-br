---
title: Objeto NetworkSettings
description: Para scripts, fornece as configurações que o serviço Agendador de Tarefas usa para obter um perfil de rede.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Objeto NetworkSettings Agendador de Tarefas
- Objeto NetworkSettings Agendador de Tarefas , descrito
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc5e247ad3de50268c6075f8956687f92800c4e901788b5098a0cef868bb202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759688"
---
# <a name="networksettings-object"></a>Objeto NetworkSettings

Para scripts, fornece as configurações que o serviço Agendador de Tarefas usa para obter um perfil de rede.

## <a name="members"></a>Membros

O **objeto NetworkSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto NetworkSettings** tem essas propriedades.



| Propriedade                                        | Tipo de acesso           | Descrição                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Id**](networksettings-id.md)<br/>     | Leitura/gravação<br/> | Obtém ou define um valor guid que identifica um perfil de rede.<br/>                        |
| [**Nome**](networksettings-name.md)<br/> | Leitura/gravação<br/> | Obtém ou define o nome de um perfil de rede. O nome é usado para fins de exibição. <br/> |



 

## <a name="remarks"></a>Comentários

Ao ler ou escrever seu próprio XML para uma tarefa, as configurações de rede são especificadas usando o [**elemento NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) do Agendador de Tarefas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas objetos](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





