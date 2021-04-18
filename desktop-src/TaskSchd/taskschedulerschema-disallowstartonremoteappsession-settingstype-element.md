---
title: Elemento DisallowStartOnRemoteAppSession (settingstype)
description: Especifica que a tarefa não será iniciada se for disparada para execução em uma sessão integrada de aplicativos remotos (trilho).
ms.assetid: 8323d8d9-fb6a-4876-9967-cc2344c77de3
keywords:
- Agendador de Tarefas do elemento DisallowStartOnRemoteAppSession
topic_type:
- apiref
api_name:
- DisallowStartOnRemoteAppSession
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11e3d0a367f2385e78cf1ec56231bbf7632fe05b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796307"
---
# <a name="disallowstartonremoteappsession-settingstype-element"></a>Elemento DisallowStartOnRemoteAppSession (settingstype)

Especifica que a tarefa não será iniciada se for disparada para execução em uma sessão integrada de aplicativos remotos (trilho).

``` syntax
<xs:element name="DisallowStartOnRemoteAppSession"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

O elemento **DisallowStartOnRemoteAppSession** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

A configuração padrão para esse elemento é false.

Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**ITaskSettings2::D isallowstartonremoteappsession**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_disallowstartonremoteappsession) .

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento Settings que não permite que a tarefa seja iniciada se a tarefa for disparada para ser executada em uma sessão de trilho.


```XML
<Settings>
    <DisallowStartOnRemoteAppSession>true</DisallowStartOnRemoteAppSession>
</Settings>
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





