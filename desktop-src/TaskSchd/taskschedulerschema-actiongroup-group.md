---
title: grupo actionGroup
description: Define o grupo de ações que uma tarefa pode executar.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- grupos actionGroup Agendador de Tarefas
- actionGroup Agendador de Tarefas
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcfd37187373e8bebdcc6b2af22323fd5475a6893791158b83b16c278752e420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357169"
---
# <a name="actiongroup-group"></a>grupo actionGroup

Define o grupo de ações que uma tarefa pode executar.

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                    | Type                                                                       | Descrição                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Representa uma ação que dispara um manipulador.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Representa uma ação que executa uma operação de linha de comando.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Representa uma ação que envia uma mensagem de email.<br/>            |
| [**Showmessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Representa uma ação que mostra uma caixa de mensagem.<br/>               |



## <a name="remarks"></a>Comentários

Ao ler ou escrever XML, os elementos definidos por esse grupo são os elementos filho do [**elemento**](taskschedulerschema-actions-tasktype-element.md) Actions.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





