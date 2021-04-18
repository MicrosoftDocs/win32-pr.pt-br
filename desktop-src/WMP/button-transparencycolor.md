---
title: BUTTON. transparencyColor
description: O atributo transparencyColor especifica ou recupera a cor que será transparente nas imagens de botão.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON. transparencyColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784910"
---
# <a name="buttontransparencycolor"></a>BUTTON. transparencyColor

O atributo **transparencyColor** especifica ou recupera a cor que será transparente nas imagens de **botão** .

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação sem padrão contendo um dos valores a seguir.



| Valor                                    | Descrição                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Automático                                     | A cor do pixel no local 0, 0 na imagem torna-se a cor transparente.                        |
| Qualquer valor de formato de cor do Internet Explorer | Um valor de formato de cor do Internet Explorer se torna a cor transparente (por exemplo, "vermelho" ou " \# FF0000"). |
| Nenhum                                     | Sem transparência.                                                                                          |



 

## <a name="remarks"></a>Comentários

Uma cor transparente em uma imagem permite que tudo esteja atrás da imagem para mostrar as áreas transparentes. O **botão** ainda receberá cliques na região transparente.

A cor transparente pode ser qualquer valor de cor do Internet Explorer. Se o valor do atributo **transparencyColor** for definido como "auto", a cor do pixel no local 0, 0 na imagem, será usada.

Se a cor especificada não for uma das cores válidas do IE, o valor anterior será mantido.

Como JPGs são derrotas e, portanto, sujeitos à alteração de cor inesperada, eles não são recomendados quando **transparencyColor** é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÃO. imagem**](button-image.md)
</dt> <dt>

[**Referência de cor**](color-reference.md)
</dt> </dl>

 

 





