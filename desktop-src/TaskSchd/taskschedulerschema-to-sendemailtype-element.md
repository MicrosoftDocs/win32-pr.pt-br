---
title: Para o elemento (sendEmailType)
description: Contém os endereços de email para os quais o email será enviado.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- Para o elemento Agendador de Tarefas
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2367686e308eb33287dafc3ce274d039b71534048fea07bc313e0542af4e2041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355636"
---
# <a name="to-sendemailtype-element"></a>Para o elemento (sendEmailType)

Contém os endereços de email para os quais o email será enviado.

``` syntax
<xs:element name="To"
    type="string"
 />
```

O elemento **to** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                              | Derivado de                                                           | Descrição                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (The Action)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa uma ação que envia uma mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**a propriedade de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).

Para o desenvolvimento de scripts, consulte [**EmailAction.to**](emailaction-to.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





