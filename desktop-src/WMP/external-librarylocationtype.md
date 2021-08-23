---
title: External.libraryLocationType
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External.libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- External.libraryLocationType Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e254ce6258cf667884e2815508b413ed1455b1b6924bfebb4edc900da048c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736196"
---
# <a name="externallibrarylocationtype"></a>External.libraryLocationType

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A **propriedade libraryLocationType** recupera [uma](library-location-constants.md) constante de local da biblioteca que indica o tipo da exibição atual no Windows Media Player.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de **caracteres** somente leitura que contém uma das constantes de local da biblioteca.

## <a name="remarks"></a>Comentários

Essa propriedade funciona em combinação com a [propriedade External.libraryLocationID.](external-librarylocationid.md) Por exemplo, suponha **que libraryLocationType** seja igual a CPAlbumID e **libraryLocationID** seja igual a 3. Isso significa que a exibição atual Windows Media Player mostra o álbum que tem uma ID de 3. Para obter mais informações sobre como Windows Media Player visualizações do conteúdo da loja online, consulte [Local e Item Selecionado.](location-and-selected-item.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para lojas online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**Local e Item Selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 





