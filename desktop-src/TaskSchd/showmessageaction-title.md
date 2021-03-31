---
title: Propriedadeprovider. title
description: Para scripts, Obtém ou define o título da caixa de mensagem.
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- Agendador de Tarefas de propriedade de título
- Propriedade Title Agendador de Tarefas, objeto exmessageaction
- Agendador de Tarefas do objeto exmessageaction, Propriedade Title
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644425"
---
# <a name="showmessageactiontitle-property"></a>Propriedadeprovider. title

\[Não há mais suporte para este objeto. Você pode usar o IExecAction com a função script do Windows [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) para mostrar uma mensagem na sessão do usuário.\]

Para scripts, Obtém ou define o título da caixa de mensagem.

## <a name="syntax"></a>Sintaxe


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a>Valor da propriedade

O título da caixa de mensagem.

## <a name="remarks"></a>Comentários

Cadeias de caracteres com parâmetros podem ser usadas no texto do título da caixa de mensagem. Para obter mais informações, consulte a seção de exemplos em [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).

Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll. Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso. O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso. Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                    |
| Fim do suporte do servidor<br/>    | Windows Server 2008 R2<br/>                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Permessageaction**](showmessageaction.md)
</dt> </dl>

 

