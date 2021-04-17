---
title: Elemento body (sendEmailType)
description: Contém o texto no corpo da mensagem de email.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Elemento de corpo Agendador de Tarefas
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760142"
---
# <a name="body-sendemailtype-element"></a>Elemento body (sendEmailType)

Contém o texto no corpo da mensagem de email.

``` syntax
<xs:element name="Body"
    type="string"
 />
```

O elemento **Body** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                              | Derivado de                                                           | Descrição                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (The Action)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa uma ação que envia uma mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade Body de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).

Para desenvolvimento de script, consulte [**emailaction. Body**](emailaction-body.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





