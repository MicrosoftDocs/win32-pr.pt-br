---
title: Elemento ShowMessage (actionGroup)
description: Representa uma ação que mostra uma caixa de mensagem.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Elemento ShowMessage Agendador de Tarefas
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474bc44550408591616d3a8d2c6c3c69a5a0d073c90297c60b4a831627c996e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611294"
---
# <a name="showmessage-actiongroup-element"></a>Elemento ShowMessage (actionGroup)

Representa uma ação que mostra uma caixa de mensagem.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

O **elemento ShowMessage** é definido pelo [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                    | Derivado de                                                       | Descrição                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Ações (taskType)**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contém as ações executadas pela tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                            | Type           | Descrição                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Corpo**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Especifica o texto a ser exibido no corpo da caixa de mensagem. <br/> |
| [**Título**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Especifica o título da caixa de mensagem. <br/>                       |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, uma ação de caixa de mensagem é especificada usando o [**objeto ShowMessageAction.**](showmessageaction.md)

Para desenvolvimento em C++, uma ação de caixa de mensagem é especificada usando a interface [**IShowMessageAction.**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)

**Windows 8 e Windows Server 2012:** Esse elemento foi removido. Você pode usar IExecAction com a função Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) de script para mostrar uma mensagem na sessão do usuário.

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que usa uma ação de caixa de mensagem, consulte [Exemplo de caixa de mensagem (XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                 |
| Fim do suporte ao servidor<br/>    | Windows Server 2008 R2<br/>                    |



 

