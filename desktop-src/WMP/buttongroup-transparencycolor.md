---
title: BUTTON. transparencyColor
description: O atributo transparencyColor especifica ou recupera a cor transparente das imagens de um botão.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- TransparencyColor Windows Media Player.
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaf6fb70db7d2699a63eb7b4fd34009f7b8ba75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794505"
---
# <a name="buttongrouptransparencycolor"></a>BUTTON. transparencyColor

O atributo **transparencyColor** especifica ou recupera a cor transparente das imagens de um **botão** .

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação sem padrão, contendo um dos valores a seguir.



| Valor                                       | Descrição                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Automático                                        | O pixel no local 0, 0 na imagem torna-se a cor transparente.                              |
| qualquer valor de cor do Microsoft Internet Explorer | Um valor de cor do Internet Explorer se torna a cor transparente (por exemplo, "vermelho" ou " \# FF0000"). |
| Nenhum                                        | Padrão. Sem transparência.                                                                          |



 

## <a name="remarks"></a>Comentários

Uma cor transparente em uma imagem permitirá que tudo esteja atrás da imagem para mostrar as áreas de transparência. A região transparente é clicável, a menos que recortada pela marca **clippingImage** .

A cor pode ser qualquer valor de cor do Microsoft Internet Explorer. Se o valor for auto, a cor do pixel no local 0, 0 na imagem, será usada.

Se a cor especificada não for uma das cores válidas do Internet Explorer, um aviso será retornado e o valor anterior será mantido.

Como JPGs são derrotas e, portanto, sujeitos à alteração de cor inesperada, eles não são recomendados quando **transparencyColor** é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de botão**](buttongroup-element.md)
</dt> <dt>

[**Referência de cor**](color-reference.md)
</dt> </dl>

 

 





