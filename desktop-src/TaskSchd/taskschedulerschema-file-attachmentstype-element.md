---
title: Elemento File (AttachmentType)
description: Contém o caminho para um arquivo enviado como um anexo em uma mensagem de email.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Elemento de arquivo Agendador de Tarefas
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369468"
---
# <a name="file-attachmentstype-element"></a>Elemento File (AttachmentType)

Contém o caminho para um arquivo enviado como um anexo em uma mensagem de email.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

O elemento **File** é definido pelo tipo complexo [**AttachmentType**](taskschedulerschema-attachmentstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                      | Derivado de                                                               | Descrição                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Anexos (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**AttachmentType**](taskschedulerschema-attachmentstype-complextype.md) | Contém uma lista de anexos na mensagem de email.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Para desenvolvimento de script, consulte [**emailaction. Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





