---
title: External. selectedItemid
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. selectedItemid
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- External. selectedItemid Windows Media Player
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
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760065"
---
# <a name="externalselecteditemid"></a>External. selectedItemid

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **selecteditemid** recupera o identificador do item de mídia selecionado no momento no Windows Media Player.

## <a name="syntax"></a>Syntax

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

Essa propriedade é usada em combinação com a propriedade [external. selecteditemtype](external-selecteditemtype.md) . Por exemplo, se **selecteditemtype** for igual a CPTrackID, **selecteditemid** será a ID da faixa selecionada. Para obter mais informações sobre como o Windows Media Player caracteriza exibições de conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).

Determinadas exibições no Windows Media Player têm um item de mídia específico selecionado. Por exemplo, suponha que a exibição atual represente um álbum. Um álbum é um contêiner de faixas, portanto **selecteditemtype** é igual a CPTrackID e **selecteditemid** é a ID da faixa selecionada. Outras exibições não têm um item de mídia selecionado. Por exemplo, se o usuário clicar no nó raiz do armazenamento online no controle de exibição de árvore, o Windows Media Player exibirá uma página de descoberta fornecida pela loja online. O Player não exibe nenhum contêiner de itens de mídia na interface do usuário do Player. Nesse caso, **selecteditemtype** é igual a UnknownLocation e **selecteditemid** é igual à cadeia de caracteres vazia.

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

 

 





