---
title: Elemento Title (showMessageType)
description: Contém o título da caixa de mensagem.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Elemento Title Agendador de Tarefas
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e5fe72b791a963e78d49ace14f7edec1210dc3bf23a5f7cee9550e6f6db53e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355673"
---
# <a name="title-showmessagetype-element"></a>Elemento Title (showMessageType)

Contém o título da caixa de mensagem.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

O **elemento Title** é definido pelo tipo complexo [**showMessageType.**](taskschedulerschema-showmessagetype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                  | Derivado de                                                               | Descrição                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Representa uma ação que mostra uma caixa de mensagem.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade Title de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).

Para desenvolvimento de scripts, [**consulte ShowMessageAction.Title**](showmessageaction-title.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





