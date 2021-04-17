---
title: CUSTOMSLIDER. Image
description: O atributo Image especifica ou recupera o nome do arquivo que contém as imagens correspondentes aos vários Estados do controle deslizante personalizado.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- CUSTOMSLIDER. Image Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762087"
---
# <a name="customsliderimage"></a>CUSTOMSLIDER. Image

O atributo **Image** especifica ou recupera o nome do arquivo que contém as imagens correspondentes aos vários Estados do controle deslizante personalizado.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

O atributo **Image** é obrigatório. Ele especifica um arquivo de imagem que consiste em uma ou mais subimagems, organizadas horizontal ou verticalmente, representando os vários Estados do controle deslizante personalizado. Cada subimagem deve ter as mesmas dimensões que o **positionImage** ou o controle deslizante personalizado não funcionará corretamente. A altura ou a largura da imagem geral deve, portanto, ser um múltiplo par da altura ou largura do **positionImage**.

Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados).

## <a name="examples"></a>Exemplos

Veja a seguir um exemplo de uma imagem de controle deslizante personalizado. O **positionImage** correspondente é mostrado na seção de exemplo da propriedade **positionImage** .

![imagem customslider de exemplo](images/dial.png)

O atributo **positionImage** também contém um exemplo de código que ilustra como os atributos do elemento **CUSTOMSLIDER** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





