---
title: External.libraryLocationID
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External.libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- External.libraryLocationID Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65119db42e8a4d6a06414f1c7790fb8716c0f9423391ed0a58f74a6913cb3b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649126"
---
# <a name="externallibrarylocationid"></a>External.libraryLocationID

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A **propriedade libraryLocationID** recupera o identificador do item de mídia específico exibido atualmente na exibição do Player.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres somente **leitura.**

## <a name="remarks"></a>Comentários

Essa propriedade funciona em combinação com a [propriedade External.libraryLocationType.](external-librarylocationtype.md) Por exemplo, suponha **que libraryLocationType** seja igual a CPAlbumID e **libraryLocationID** seja igual a 3. Isso significa que a exibição atual Windows Media Player mostra o álbum que tem uma ID de 3. Para obter mais informações sobre como Windows Media Player visualizações do conteúdo da loja online, consulte [Local e Item Selecionado.](location-and-selected-item.md)

Determinadas exibições Windows Media Player estão associadas a um item de mídia específico. Por exemplo, se a exibição atual representar um álbum individual, **libraryLocationType** será igual a CPAlbumID e **libraryLocationID** será a ID do álbum. Outras exibições não estão associadas a nenhum item de mídia específico. Por exemplo, se a exibição atual representar todos os álbums, **libraryLocationType** será igual a AllCPAlbumIDs, mas não haverá nenhum valor significativo que possa ser atribuído a **libraryLocationID.** Nos casos em que **a propriedade libraryLocationID** não tem nenhum valor significativo, ela é igual à cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**Local e Item Selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 





