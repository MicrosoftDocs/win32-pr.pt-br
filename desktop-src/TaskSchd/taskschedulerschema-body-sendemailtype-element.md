---
title: Elemento Body (sendEmailType)
description: Contém o texto no corpo da mensagem de email.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Elemento Body Agendador de Tarefas
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a924062b3a382bc8362bdfa45e1477b4e841222bdd1f5ac70fbb8adbc9b070b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857959"
---
# <a name="body-sendemailtype-element"></a>Elemento Body (sendEmailType)

Contém o texto no corpo da mensagem de email.

``` syntax
<xs:element name="Body"
    type="string"
 />
```

O **elemento Body** é definido pelo tipo complexo [**sendEmailType.**](taskschedulerschema-sendemailtype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                              | Derivado de                                                           | Descrição                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa uma ação que envia uma mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade body de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).

Para desenvolvimento de scripts, [**consulte EmailAction.Body**](emailaction-body.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





