---
title: External. libraryLocationType
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- Windows Media Player externo. libraryLocationType
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
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770490"
---
# <a name="externallibrarylocationtype"></a>External. libraryLocationType

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **libraryLocationType** recupera uma [constante de local de biblioteca](library-location-constants.md) que indica o tipo da exibição atual no Windows Media Player.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** somente leitura que contém uma das constantes de localização da biblioteca.

## <a name="remarks"></a>Comentários

Essa propriedade funciona em combinação com a propriedade [external. libraryLocationID](external-librarylocationid.md) . Por exemplo, suponha que **libraryLocationType** seja igual a CPAlbumID e **libraryLocationID** seja igual a 3. Isso significa que a exibição atual no Windows Media Player está mostrando o álbum que tem uma ID de 3. Para obter mais informações sobre como o Windows Media Player caracteriza exibições de conteúdo da loja online, consulte [local e item selecionado](location-and-selected-item.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**Local e item selecionado**](location-and-selected-item.md)
</dt> </dl>

 

 





