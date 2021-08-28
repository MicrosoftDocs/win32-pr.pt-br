---
title: Elemento File (attachmentsType)
description: Contém o caminho para um arquivo enviado como um anexo em uma mensagem de email.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Elemento file Agendador de Tarefas
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 793b23bc6b9d75ac809c42063fa9c300542705b718cd22253f6f2d3a1a76caa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125846"
---
# <a name="file-attachmentstype-element"></a>Elemento File (attachmentsType)

Contém o caminho para um arquivo enviado como um anexo em uma mensagem de email.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

O **elemento File** é definido pelo tipo complexo [**attachmentsType.**](taskschedulerschema-attachmentstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                      | Derivado de                                                               | Descrição                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Anexos (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) | Contém uma lista de anexos na mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Para desenvolvimento de scripts, [**consulte EmailAction.Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





