---
title: Elemento BCC (sendEmailType)
description: Contém os endereços de email usados na linha Cco de uma mensagem de email.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Agendador de Tarefas do elemento BCC
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085779"
---
# <a name="bcc-sendemailtype-element"></a>Elemento BCC (sendEmailType)

Contém os endereços de email usados na linha Cco de uma mensagem de email.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

O elemento **BCC** é definido pelo tipo complexo [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                              | Derivado de                                                           | Descrição                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (The Action)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Representa uma ação que envia uma mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade BCC de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).

Para desenvolvimento de script, consulte [**emailaction. Bcc**](emailaction-bcc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





