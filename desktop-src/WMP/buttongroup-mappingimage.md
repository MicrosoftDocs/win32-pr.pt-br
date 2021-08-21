---
title: BUTTONGROUP.mappingImage
description: O atributo mappingImage especifica ou recupera o nome da imagem que representa o mapa de botão do BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- BUTTONGROUP.mappingImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c26a920042aae4ba144f194845f350030f5675c1b9cc3fcfed552346904add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119887"
---
# <a name="buttongroupmappingimage"></a>BUTTONGROUP.mappingImage

O **atributo mappingImage** especifica ou recupera o nome da imagem que representa o mapa de botão do **BUTTONGROUP.**

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Esse é um atributo obrigatório que deve ser especificado.

A imagem de mapeamento deve ter as mesmas dimensões que a imagem **principal.** É um mapa das áreas clicáveis da imagem principal. Construa o mapa preenchendo cada área clicável com uma cor diferente.

Ao definir cada **BUTTONELEMENT**, designe sua cor do mapa usando o **atributo mappingColor.** Por exemplo, se você tiver um gráfico de botão em forma de sinal de parada na imagem principal, poderá criar um mapa com a área do sinal vermelho colorido. O **atributo BUTTONELEMENT** deve ser especificado como vermelho para tornar a imagem de sinal de parada clicável.

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF (sem incluir GIFs animados). Como os JPGs são com perda e, portanto, estão sujeitos a alterações de cor inesperadas, eles não são recomendados para mapear imagens.

## <a name="examples"></a>Exemplos

A ilustração a seguir é um exemplo de **mappingImage** e a imagem visível à que ele corresponde. Essas imagens fazem parte da capa na pasta Tiny incluída no SDK.

![imagem de mapeamento de exemplo](images/absam01m.png)![imagem de plano de fundo de exemplo](images/absam01f.png)

Consulte *BUTTONELEMENT*. [Atributo mappingColor](buttonelement-mappingcolor.md) para um exemplo de código que ilustra o uso desse atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





