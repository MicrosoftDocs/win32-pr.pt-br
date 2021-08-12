---
title: Elemento Subject (sendEmailType)
description: Contém o assunto da mensagem de email.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Elemento subject Agendador de Tarefas
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15bf3c84befd9dd8f4c9c4a544fc920b7066184c6bf367c404bb14f22f573b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611184"
---
# <a name="subject-sendemailtype-element"></a>Elemento Subject (sendEmailType)

Contém o assunto da mensagem de email.

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

O **elemento Subject** é definido pelo tipo complexo [**sendEmailType.**](taskschedulerschema-sendemailtype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                              | Derivado de                                                           | Descrição                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa uma ação que envia uma mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade de assunto de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).

Para desenvolvimento de scripts, [**consulte EmailAction.Subject.**](emailaction-subject.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





