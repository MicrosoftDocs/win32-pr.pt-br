---
title: Elemento from (sendEmailType)
description: Contém o endereço de email do remetente do email.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- Do elemento Agendador de Tarefas
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009154"
---
# <a name="from-sendemailtype-element"></a>Elemento from (sendEmailType)

Contém o endereço de email do remetente do email.

``` syntax
<xs:element name="From"
    type="string"
 />
```

O elemento **from** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                              | Derivado de                                                           | Descrição                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (The Action)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa uma ação que envia uma mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**da propriedade de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).

Para desenvolvimento de script, consulte [**emailaction. de**](emailaction-from.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





