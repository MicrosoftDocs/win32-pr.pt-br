---
title: External.selectedItemType
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External.selectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- External.selectedItemType Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb58b13f1486bb30a79cd20e2f43f715df694f661c7b56e5eadd29f0c5c06c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648410"
---
# <a name="externalselecteditemtype"></a>External.selectedItemType

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A **propriedade selectedItemType** recupera o tipo do item de mídia selecionado no momento Windows Media Player.

## <a name="syntax"></a>Syntax

window.external.selectedItemType()

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de **caracteres** somente leitura que contém uma das [constantes de local da biblioteca](library-location-constants.md).

## <a name="remarks"></a>Comentários

Essa propriedade é usada em combinação com a **propriedade External.selectedItemID.** Por exemplo, se **selectedItemType** for igual a CPTrackID, **selectedItemID** será a ID da faixa selecionada. Para obter mais informações sobre como Windows Media Player visualizações do conteúdo da loja online, consulte [Local e Item Selecionado.](location-and-selected-item.md)

Determinadas exibições Windows Media Player têm um item de mídia específico selecionado. Por exemplo, suponha que a exibição atual representa um álbum. Um álbum é um contêiner de faixas, portanto **selectedItemType** é igual a CPTrackID e **selectedItemID** é a ID da faixa selecionada. Outras exibições não têm um item de mídia selecionado. Por exemplo, se o usuário clicar no nó raiz da loja online no controle de exibição de árvore, o Windows Media Player exibirá uma página de descoberta fornecida pela loja online. O Player não exibe nenhum contêiner de itens de mídia na interface do usuário do Player. Nesse caso, **selectedItemType** é igual a UnknownLocation e **selectedItemID** é igual à cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.selectedItemID**](external-selecteditemid.md)
</dt> <dt>

[**Local e Item Selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 





