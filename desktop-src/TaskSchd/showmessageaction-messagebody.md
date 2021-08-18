---
title: Propriedade ShowMessageAction.MessageBody
description: Para scripts, obtém ou define o texto da mensagem exibido no corpo da caixa de mensagem.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- Propriedade MessageBody Agendador de Tarefas
- Propriedade MessageBody Agendador de Tarefas objeto , ShowMessageAction
- Objeto ShowMessageAction Agendador de Tarefas propriedade , MessageBody
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5b408ad8642cc17b85d783a8f26d7de3322a26309897e4d9b3c128401449d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139339"
---
# <a name="showmessageactionmessagebody-property"></a>Propriedade ShowMessageAction.MessageBody

\[Não há mais suporte para esse objeto. Você pode usar IExecAction com a função Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) de script para mostrar uma mensagem na sessão do usuário.\]

Para scripts, obtém ou define o texto da mensagem exibido no corpo da caixa de mensagem.

## <a name="syntax"></a>Syntax


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a>Valor da propriedade

O texto da mensagem exibido no corpo da caixa de mensagem.

## <a name="remarks"></a>Comentários

Cadeias de caracteres parametrizadas podem ser usadas no texto da mensagem da caixa de mensagem. Para obter mais informações, consulte a seção Exemplos [**em EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).

Ao definir esse valor de propriedade, o valor pode ser texto recuperado de um arquivo de .dll recurso. Uma cadeia de caracteres especializada é usada para referenciar o texto do arquivo de recurso. O formato da cadeia de caracteres é $(@ Dll , ResourceID ) em que Dll é o caminho para o arquivo .dll que contém o recurso e ResourceID é o identificador do texto \[ \] do \[ \] \[ \] \[ \] recurso. Por exemplo, a definição desse valor da propriedade como $(@ %SystemRoot% System32ResourceName.dll, -101) definirá a propriedade como o valor do texto do recurso com um identificador igual \\ \\ a -101 no arquivo %SystemRoot% \\ System32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                    |
| Fim do suporte ao servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> </dl>

 

