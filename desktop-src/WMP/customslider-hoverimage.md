---
title: CUSTOMSLIDER.hoverImage
description: O atributo hoverImage especifica ou recupera a imagem que aparece quando o mouse está sobre o controle deslizante personalizado.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- CUSTOMSLIDER. hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d12f337c8d4889e0d2e94bac0c0a4dce74f3a80fda9261d245b91ce5612754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651396"
---
# <a name="customsliderhoverimage"></a>CUSTOMSLIDER.hoverImage

O atributo **hoverImage** especifica ou recupera a imagem que aparece quando o mouse está sobre o controle deslizante personalizado.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Se não for especificado, o arquivo especificado no atributo **Image** será usado.

O **hoverImage** representa o estado de foco do controle CUSTOMSLIDER; ou seja, o estado mostrado quando o cursor do mouse passa sobre ele. Pode ser uma única imagem ou uma série de imagens que representam os vários Estados do controle deslizante. Se várias imagens forem usadas, elas serão organizadas da mesma maneira que o arquivo de **imagem**

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

 

 





