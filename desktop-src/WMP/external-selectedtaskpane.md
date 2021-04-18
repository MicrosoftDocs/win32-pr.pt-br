---
title: External. SelectedTaskPane
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade SelectedTaskPane especifica ou recupera o painel de tarefas selecionado no momento.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- Windows Media Player externo. SelectedTaskPane
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800132"
---
# <a name="externalselectedtaskpane"></a>External. SelectedTaskPane

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **SelectedTaskPane** especifica ou recupera o painel de tarefas selecionado no momento.

## <a name="syntax"></a>Syntax

janela. external. SelectedTaskPane = *tarefa*

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** de leitura/gravação. Os valores possíveis são "ServiceTask1", "ServiceTask2" e "ServiceTask3".

## <a name="remarks"></a>Comentários

A especificação de um valor para essa propriedade realça o botão para esse painel. Ele não torna o painel de tarefas especificado ativo. Você deve especificar um valor para essa propriedade para definir o botão do painel de tarefas atual para sua página da Web quando a página for carregada para garantir que o botão correto do painel de tarefas esteja ativo.

Para tornar um painel de tarefas específico o ativo, use o método **NavigateTaskPaneURL** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





