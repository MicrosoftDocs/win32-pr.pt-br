---
title: External. selectedItemid
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. selectedItemid
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- Windows Media Player externa. selectedItemid
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea4b93656adc3fab25ab96e41fe417bde158035c5c11a0af9be84c5d555b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648426"
---
# <a name="externalselecteditemid"></a>External. selectedItemid

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **selecteditemid** recupera o identificador do item de mídia selecionado no momento em Windows Media Player.

## <a name="syntax"></a>Syntax

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

Essa propriedade é usada em combinação com a propriedade [external. selecteditemtype](external-selecteditemtype.md) . Por exemplo, se **selecteditemtype** for igual a CPTrackID, **selecteditemid** será a ID da faixa selecionada. para obter mais informações sobre como Windows Media Player caracteriza as exibições do conteúdo da loja online, consulte [local e Item selecionado](location-and-selected-item.md).

determinadas exibições em Windows Media Player têm um item de mídia específico selecionado. Por exemplo, suponha que a exibição atual represente um álbum. Um álbum é um contêiner de faixas, portanto **selecteditemtype** é igual a CPTrackID e **selecteditemid** é a ID da faixa selecionada. Outras exibições não têm um item de mídia selecionado. por exemplo, se o usuário clicar no nó raiz do armazenamento online no controle de exibição de árvore, Windows Media Player exibirá uma página de descoberta fornecida pela loja online. O Player não exibe nenhum contêiner de itens de mídia na interface do usuário do Player. Nesse caso, **selecteditemtype** é igual a UnknownLocation e **selecteditemid** é igual à cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. selectedItemtype**](external-selecteditemtype.md)
</dt> <dt>

[**Local e item selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 





