---
title: Elemento Cc (sendEmailType)
description: Contém os endereços de email usados na linha Cc de uma mensagem de email.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Elemento Cc Agendador de Tarefas
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b639116a514a48eeab35561d936b6e5b8a4b479a9f8f0f09b6d1b596bd5e4bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334605"
---
# <a name="cc-sendemailtype-element"></a>Elemento Cc (sendEmailType)

Contém os endereços de email usados na linha Cc de uma mensagem de email.

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

O **elemento Cc** é definido pelo tipo complexo [**sendEmailType.**](taskschedulerschema-sendemailtype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                              | Derivado de                                                           | Description                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa uma ação que envia uma mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade Cc de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).

Para desenvolvimento de script, [**consulte EmailAction.Cc**](emailaction-cc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





