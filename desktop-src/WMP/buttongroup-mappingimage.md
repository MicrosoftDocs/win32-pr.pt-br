---
title: BUTTON. mappingImage
description: O atributo mappingImage especifica ou recupera o nome da imagem que representa o mapa de botão do botão.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- MappingImage Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760277"
---
# <a name="buttongroupmappingimage"></a>BUTTON. mappingImage

O atributo **mappingImage** especifica ou recupera o nome da imagem que representa o mapa de botão do **botão**.

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Este é um atributo obrigatório que deve ser especificado.

A imagem de mapeamento deve ter as mesmas dimensões que a **imagem** principal. É um mapa das áreas clicáveis da imagem principal. Construa o mapa preenchendo cada área clicável com uma cor diferente.

Ao definir cada **buttonelement**, designe sua cor a partir do mapa usando o atributo **mappingColor** . Por exemplo, se você tiver um gráfico de botão de sinal de parada na imagem principal, poderá criar um mapa com a área do sinal vermelho. O atributo **buttonelement** deve ser especificado como vermelho para tornar a imagem de parada-assinatura clicável.

Os formatos de imagem com suporte são BMP, JPG, PNG e GIF (não incluindo GIFs animados). Como JPGs são derrotas e, portanto, sujeitos à alteração de cor inesperada, eles não são recomendados para mapear imagens.

## <a name="examples"></a>Exemplos

A ilustração a seguir é um exemplo de um **mappingImage** e a imagem visível à qual ele corresponde. Essas imagens fazem parte da capa na pequena pasta incluída no SDK.

![exemplo de imagem de mapeamento](images/absam01m.png)![imagem de plano de fundo de exemplo](images/absam01f.png)

Consulte o *botãoelement*. atributo [mappingColor](buttonelement-mappingcolor.md) para um exemplo de código que ilustra o uso desse atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BUTTONelement. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**Elemento de botão**](buttongroup-element.md)
</dt> <dt>

[**BUTTON. Image**](buttongroup-image.md)
</dt> <dt>

[**BUTTON. transparencyColor**](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





