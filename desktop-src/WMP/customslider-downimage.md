---
title: CUSTOMSLIDER.downImage
description: O atributo downImage especifica ou recupera a imagem de estado inferior do controle deslizante personalizado.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- CUSTOMSLIDER. downImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8365043654bc3cca9fbf79162302cf804155956d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794494"
---
# <a name="customsliderdownimage"></a>CUSTOMSLIDER.downImage

O atributo **downImage** especifica ou recupera a imagem de estado inferior do controle deslizante personalizado.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Se não for especificado, o arquivo especificado no atributo **Image** será usado.

O **downImage** representa o estado inoperante do controle **CUSTOMSLIDER** . Pode ser uma única imagem ou uma série de imagens que representam os vários Estados do controle deslizante. Se várias imagens forem usadas, elas serão organizadas da mesma maneira que o arquivo de **imagem** .

Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. Image**](customslider-image.md)
</dt> </dl>

 

 





