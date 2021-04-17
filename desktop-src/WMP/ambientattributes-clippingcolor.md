---
title: Ambienteattributes. clippingColor
description: O atributo clippingColor especifica ou recupera a cor a ser recortada do bitmap clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- ClippingColor do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762112"
---
# <a name="ambientattributesclippingcolor"></a>Ambienteattributes. clippingColor

O atributo **clippingColor** especifica ou recupera a cor a ser recortada do bitmap **clippingImage** .

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.



| Valor                                       | Descrição                                       |
|---------------------------------------------|---------------------------------------------------|
| Automático                                        | Padrão. A cor no local do pixel 0, 0 é usada. |
| qualquer valor de cor do Microsoft Internet Explorer | A cor especificada do Internet Explorer é usada.    |



 

## <a name="remarks"></a>Comentários

A cor de recorte indica as regiões do **clippingImage** (ou **backgroundImage** para **exibição** ou **subexibição**) que correspondem às partes transparentes e não clicáveis do controle. A cor de recorte pode indicar várias regiões a serem recortadas. Um aviso será emitido se o **clippingImage** for um jpg para avisar sobre a perda de cor em JPGs.

O atributo **clippingColor** não é suportado pelo elemento **playlist** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambienteattributes. clippingImage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**Referência de cor**](color-reference.md)
</dt> </dl>

 

 





