---
title: COLUNA. columnID
description: O atributo columnID especifica ou recupera uma ID de coluna no controle PLAYLIST.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- COLUNA. columnID Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810572"
---
# <a name="columncolumnid"></a>COLUNA. columnID

O atributo **columnid** especifica ou recupera uma ID de coluna no controle **playlist** .

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Os valores de **columnid** são os mesmos valores usados com o método **getItemInfo** em um objeto de **mídia** . Uma lista pode ser obtida usando a *mídia*. Propriedade **attributeCount** para determinar o número de atributos disponíveis para um determinado objeto de **mídia** . Os números de índice podem ser usados com a *mídia*. método **GetAttributeName** para determinar os nomes dos atributos que, por sua vez, podem ser passados para a *mídia*. **getItemInfo**. A propriedade **columnid** só pode ser definida com esses valores, com exceção de alguns valores que podem não ser retornados pela *mídia*. **GetAttributeName**. Esses valores estão listados abaixo.



| Valor     | Descrição                                                                        |
|-----------|------------------------------------------------------------------------------------|
| name      | Exibe o nome do objeto de **mídia** .                                         |
| duration  | Exibe a duração do objeto de **mídia** .                                     |
| sourceURL | Exibe a URL do objeto de **mídia** .                                          |
| status    | Exibe o status da cópia de arquivos.                                              |
| tamanho      | Exibe o tamanho do arquivo que o objeto de **mídia** representa.                |
| extensão | Exibe a extensão de nome de arquivo do arquivo que o objeto de **mídia** representa. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento COLUMN**](column-element.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> </dl>

 

 





