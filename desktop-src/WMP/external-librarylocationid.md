---
title: External. libraryLocationID
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Windows Media Player externo. libraryLocationID
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
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761445"
---
# <a name="externallibrarylocationid"></a>External. libraryLocationID

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **libraryLocationID** recupera o identificador do item de mídia específico que é exibido atualmente no modo de exibição do Player.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

Essa propriedade funciona em combinação com a propriedade [external. libraryLocationType](external-librarylocationtype.md) . Por exemplo, suponha que **libraryLocationType** seja igual a CPAlbumID e **libraryLocationID** seja igual a 3. Isso significa que a exibição atual no Windows Media Player está mostrando o álbum que tem uma ID de 3. Para obter mais informações sobre como o Windows Media Player caracteriza exibições de conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).

Determinadas exibições no Windows Media Player estão associadas a um item de mídia específico. Por exemplo, se a exibição atual representar um álbum individual, **libraryLocationType** será igual a CPAlbumID e **LIBRARYLOCATIONID** será a ID do álbum. Outras exibições não estão associadas a nenhum item de mídia específico. Por exemplo, se a exibição atual representar todos os álbuns, **libraryLocationType** será igual a AllCPAlbumIDs, mas não haverá nenhum valor significativo que possa ser atribuído a **libraryLocationID**. Nos casos em que a propriedade **libraryLocationID** não tem nenhum valor significativo, ela é igual à cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**Local e item selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 





