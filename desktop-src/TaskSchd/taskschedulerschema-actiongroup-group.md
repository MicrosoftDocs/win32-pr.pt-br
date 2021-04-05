---
title: Grupo de ações
description: Define o grupo de ações que uma tarefa pode executar.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- grupo de ações Agendador de Tarefas
- Agendador de Tarefas de forma de ação
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af06598c6eca092f474467bea16a7d7b95a9563f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644483"
---
# <a name="actiongroup-group"></a>Grupo de ações

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
| [**Commanipulador**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comhandletype**](taskschedulerschema-comhandlertype-complextype.md)   | Representa uma ação que dispara um manipulador.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**exectype**](taskschedulerschema-exectype-complextype.md)               | Representa uma ação que executa uma operação de linha de comando.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Representa uma ação que envia uma mensagem de email.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**defaultmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Representa uma ação que mostra uma caixa de mensagem.<br/>               |



## <a name="remarks"></a>Comentários

Ao ler ou gravar XML, os elementos definidos por esse grupo são os elementos filho do elemento [**Actions**](taskschedulerschema-actions-tasktype-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





