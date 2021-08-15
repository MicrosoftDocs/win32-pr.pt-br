---
title: TAMBÉM ÉGLDER.image
description: O atributo de imagem especifica ou recupera o nome do arquivo que contém as imagens correspondentes aos vários estados do controle deslizante personalizado.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- WINDOWS MEDIA PLAYER
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b169bbdcac0e251a161c8e09f352caf460280b23e0198167a641721caa6c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936240"
---
# <a name="customsliderimage"></a>TAMBÉM ÉGLDER.image

O **atributo** de imagem especifica ou recupera o nome do arquivo que contém as imagens correspondentes aos vários estados do controle deslizante personalizado.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres **de** leitura/gravação que contém o nome de um arquivo de imagem.

## <a name="remarks"></a>Comentários

O **atributo** de imagem é necessário. Ele especifica um arquivo de imagem que consiste em uma ou mais sub-imagens, organizadas horizontal ou verticalmente, representando os vários estados do controle deslizante personalizado. Cada subimagem deve ter as mesmas dimensões que **positionImage** ou o controle deslizante personalizado não funcionará corretamente. Portanto, a altura ou a largura da imagem geral deve ser um múltiplo da altura ou largura da **posiçãoImagem**.

Os tipos de arquivo de imagem com suporte são BMP, JPG, PNG e GIF (sem incluir GIFs animados).

## <a name="examples"></a>Exemplos

A seguir está um exemplo de uma imagem de controle deslizante personalizada. A **positionImage correspondente** é mostrada na seção de exemplo da **propriedade positionImage.**

![exemplo de imagem delider](images/dial.png)

O **atributo positionImage** também contém um exemplo de código que ilustra como os atributos do elemento **ATTRIBUTESLIDER** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento DESLISTADER**](customslider-element.md)
</dt> <dt>

[**TAMBÉMLLIDER.positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





