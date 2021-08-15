---
title: Elemento Documentation (registrationInfoType)
description: Especifica qualquer documentação adicional para a tarefa.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Elemento de documentação Agendador de Tarefas
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6cb8c2a78450fffa467ea659b55015f064310783ae21b067093de9473612fcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356864"
---
# <a name="documentation-registrationinfotype-element"></a>Elemento Documentation (registrationInfoType)

Especifica qualquer documentação adicional para a tarefa.

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

O elemento **Documentation** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                           | Derivado de                                                                         | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |



## <a name="remarks"></a>Comentários

Para aplicativos de script, a documentação adicional da tarefa é especificada com o uso da propriedade [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) .

Para aplicativos C++, a documentação adicional da tarefa é especificada usando o usando a propriedade [**IRegistrationInfo::D kumentace**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





