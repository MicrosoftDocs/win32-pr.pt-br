---
title: Elemento body (defaultmessagetype)
description: Contém o texto a ser exibido no corpo da caixa de mensagem.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
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
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455397"
---
# <a name="body-showmessagetype-element"></a>Elemento body (defaultmessagetype)

Contém o texto a ser exibido no corpo da caixa de mensagem.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

O elemento **Body** é definido pelo tipo complexo [**exmessagetype**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                  | Derivado de                                                               | Descrição                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Exmessage (The Action)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**defaultmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Representa uma ação que mostra uma caixa de mensagem.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade MessageBody de IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).

Para o desenvolvimento de script, consulte [**Permessageaction. MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





