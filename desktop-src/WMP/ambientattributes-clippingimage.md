---
title: Ambienteattributes. clippingImage
description: O atributo clippingImage especifica ou recupera a região para a qual o controle será recortado.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- ClippingImage do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781467"
---
# <a name="ambientattributesclippingimage"></a>Ambienteattributes. clippingImage

O atributo **clippingImage** especifica ou recupera a região para a qual o controle será recortado.

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que indica o nome do arquivo de imagem. Não tem nenhum valor padrão.

## <a name="remarks"></a>Comentários

O atributo **clippingImage** dá suporte a arquivos PNG, jpg, BMP e gif (não incluindo gifs animados). Como JPGs são derrotas e, portanto, sujeitos à alteração de cor inesperada, eles não são recomendados para imagens de recorte.

Esse atributo é útil quando você deseja exibir apenas uma parte da imagem de controle e não a área retangular inteira. O atributo **clippingColor** indica as regiões da imagem de recorte que correspondem a partes transparentes e não clicáveis do controle. Portanto, o controle pode ser de qualquer forma. Para obter melhores resultados, a imagem de recorte deve ter o mesmo tamanho da imagem de controle.

Não há suporte para o atributo **clippingImage** nos elementos **playlist**, **View** e **subview** . Uma imagem de recorte não funcionará com o elemento de **vídeo** se houver *vídeo*. **sem janela** é definido como false, nem com o elemento **Effects** , se houver *efeitos*. em **janela** é definido como true.

Como o uso de imagens de recorte impõe uma penalidade de desempenho, elas não devem ser usadas quando a eficiência é um problema.

## <a name="examples"></a>Exemplos

Consulte o atributo [buttonelement. mappingColor](buttonelement-mappingcolor.md) para obter um exemplo ilustrando o uso desse atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambienteattributes. clippingColor**](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





