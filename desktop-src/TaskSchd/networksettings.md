---
title: Objeto NetworkSettings
description: Para scripts, o fornece as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Agendador de Tarefas de objeto NetworkSettings
- Agendador de Tarefas de objeto NetworkSettings, descrito
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
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455308"
---
# <a name="networksettings-object"></a>Objeto NetworkSettings

Para scripts, o fornece as configurações que o serviço de Agendador de Tarefas usa para obter um perfil de rede.

## <a name="members"></a>Membros

O objeto **NetworkSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **NetworkSettings** tem essas propriedades.



| Propriedade                                        | Tipo de acesso           | Descrição                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Sessão**](networksettings-id.md)<br/>     | Leitura/gravação<br/> | Obtém ou define um valor de GUID que identifica um perfil de rede.<br/>                        |
| [**Nome**](networksettings-name.md)<br/> | Leitura/gravação<br/> | Obtém ou define o nome de um perfil de rede. O nome é usado para fins de exibição. <br/> |



 

## <a name="remarks"></a>Comentários

Ao ler ou gravar seu próprio XML para uma tarefa, as configurações de rede são especificadas usando o elemento [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos Agendador de Tarefas](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





