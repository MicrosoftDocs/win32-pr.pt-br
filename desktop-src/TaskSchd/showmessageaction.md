---
title: Objeto exmessageaction
description: Para scripts, representa uma ação que mostra uma caixa de mensagem quando uma tarefa é ativada.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Agendador de Tarefas de objeto do exmessageaction
- Agendador de Tarefas do objeto exmessageaction, descrito
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369402"
---
# <a name="showmessageaction-object"></a>Objeto exmessageaction

\[Não há mais suporte para este objeto. Você pode usar o IExecAction com a função script do Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar uma mensagem na sessão do usuário.\]

Para scripts, representa uma ação que mostra uma caixa de mensagem quando uma tarefa é ativada.

## <a name="members"></a>Membros

O objeto **Exmessageaction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **Exmessageaction** tem essas propriedades.



| Propriedade                                                        | Tipo de acesso           | Descrição                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Sessão**](action-id.md)<br/>                              | Leitura/gravação<br/> | Herdado do objeto de [**ação**](action.md) . Obtém ou define o identificador da ação.<br/> |
| [**MessageBody**](showmessageaction-messagebody.md)<br/> | Leitura/gravação<br/> | Obtém ou define o texto da mensagem que é exibido no corpo da caixa de mensagem.<br/>                |
| [**Título**](showmessageaction-title.md)<br/>             | Leitura/gravação<br/> | Obtém ou define o título da caixa de mensagem.<br/>                                                     |
| [**Tipo**](action-type.md)<br/>                          | Somente leitura<br/>  | Herdado do objeto de [**ação**](action.md) . Obtém o tipo da ação.<br/>               |



 

## <a name="remarks"></a>Comentários

Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo. Para definir o tipo de logon da tarefa como interativo, especifique 3 (**\_ \_ \_ token interativo de logon da tarefa**) ou 4 (**\_ \_ grupo de logon de tarefa**) na propriedade [**Logontype**](principal-logontype.md) da entidade de segurança da tarefa ou no parâmetro *Logontype* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

Ao ler ou gravar seu próprio XML para uma tarefa, uma ação da caixa de mensagem é especificada usando o elemento [**exmessage**](taskschedulerschema-showmessage-actiongroup-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte o [exemplo de caixa de mensagem (script)](/previous-versions//aa381916(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                    |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

