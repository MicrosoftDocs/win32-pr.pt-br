---
title: Ambienteattributes. horizontalAlignment
description: O atributo horizontalAlignment especifica ou recupera um valor que indica o posicionamento horizontal do controle quando a exibição ou a subexibição pai é redimensionada.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Windows Media Player de ambiente. horizontalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761124"
---
# <a name="ambientattributeshorizontalalignment"></a>Ambienteattributes. horizontalAlignment

O atributo **horizontalAlignment** especifica ou recupera um valor que indica o posicionamento horizontal do controle quando a **exibição** ou a **subexibição** pai é redimensionada.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.



| Valor   | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| esquerda    | Padrão. Mantém o posicionamento do controle em relação à esquerda da **exibição** ou da **subexibição** pai quando a exibição é redimensionada.                                                                                                                                                                                                                               |
| direita   | Mantém o posicionamento do controle em relação à direita da **exibição** ou da **subexibição** pai quando a exibição é redimensionada.                                                                                                                                                                                                                                       |
| centro  | Mantém o posicionamento do controle em relação ao centro horizontal da **exibição** ou à **subexibição** pai quando a exibição é redimensionada.                                                                                                                                                                                                                           |
| Estendi | Mantém o posicionamento do controle em relação às margens esquerda e direita da **exibição** ou **subexibição** pai quando redimensionada. O controle se ajusta para se ajustar quando a **exibição** ou a **subexibição** é ampliada. A imagem real não aumenta ou diminui, a menos que seja redimensionável, mas a área clicável aumente ou diminua se não estiver limitada por um **clippingImage**. |



 

## <a name="remarks"></a>Comentários

A menos que **horizontalAlignment** esteja definido como "Center", o controle manterá sua distância original da borda especificada ou de ambas as bordas se "Stretch" for especificado e o controle for redimensionável. Se o controle não for redimensionável e "Stretch" for especificado, a região clicável será ampliada.

Você pode definir qualquer combinação de **horizontalAlignment** e **verticalAlignment**. Por exemplo, se você quiser centralizar um controle tanto horizontal quanto verticalmente, defina horizontalAlignment = "Center" verticalAlignment = "Center".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambiente. verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**Ambienteattributes. clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





