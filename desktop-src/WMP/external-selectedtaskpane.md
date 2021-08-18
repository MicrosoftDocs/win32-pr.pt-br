---
title: External.SelectedTaskPane
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade SelectedTaskPane especifica ou recupera o painel de tarefas selecionado no momento.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- External.SelectedTaskPane Windows Media Player
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
ms.openlocfilehash: 24e49225be7bbdb5ce128a793d3c88409ef9d994ef5017c57b5f12738b62eaa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736186"
---
# <a name="externalselectedtaskpane"></a>External.SelectedTaskPane

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A **propriedade SelectedTaskPane** especifica ou recupera o painel de tarefas selecionado no momento.

## <a name="syntax"></a>Syntax

window.external.SelectedTaskPane = *servicetask*

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres de **leitura/gravação.** Os valores possíveis são "ServiceTask1", "ServiceTask2" e "ServiceTask3".

## <a name="remarks"></a>Comentários

Especificar um valor para essa propriedade realça o botão para esse painel. Ele não ativa o painel de tarefas especificado. Você deve especificar um valor para essa propriedade para definir o botão do painel de tarefas atual para sua página da Web quando a página for carregada para garantir que o botão do painel de tarefas correto está ativo.

Para tornar um painel de tarefas específico o ativo, use o **método NavigateTaskPaneURL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





