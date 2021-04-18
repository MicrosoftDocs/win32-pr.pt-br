---
title: Ambiente. verticalAlignment
description: O atributo verticalAlignment especifica ou recupera um valor que indica o posicionamento vertical do controle quando a exibição ou a subexibição pai é ampliada.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Windows Media Player de ambiente. verticalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781466"
---
# <a name="ambientattributesverticalalignment"></a>Ambiente. verticalAlignment

O atributo **verticalAlignment** especifica ou recupera um valor que indica o posicionamento vertical do controle quando a **exibição** ou a **subexibição** pai é ampliada.

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.



| Valor   | Descrição                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | Padrão. Mantém o posicionamento do controle em relação à parte superior da **exibição** ou da **subexibição** pai quando a exibição é redimensionada.                                                                                                                                                                                                             |
| parte inferior  | Mantém o posicionamento do controle em relação à parte inferior da **exibição** ou da **subexibição** pai quando a exibição é redimensionada.                                                                                                                                                                                                                   |
| centro  | Mantém o posicionamento do controle em relação ao centro vertical da **exibição** ou à **subexibição** pai quando a exibição é redimensionada.                                                                                                                                                                                                          |
| Estendi | Mantém o posicionamento do controle em relação às margens superior e inferior da exibição quando redimensionada. O controle se ajusta para se ajustar quando a **exibição** ou a **subexibição** pai é ampliada. A imagem real não aumenta ou diminui, a menos que seja redimensionável, mas a área clicável aumente ou diminua se não estiver limitada por um **clippingImage**. |



 

## <a name="remarks"></a>Comentários

A menos que o **verticalAlignment** esteja definido como "Center", o controle retém sua distância original da borda especificada ou de ambas as bordas se "Stretch" for especificado e o controle for redimensionável. Se o controle não for redimensionável e "Stretch" for especificado, a região clicável será ampliada.

Você pode definir qualquer combinação dos atributos **horizontalAlignment** e **verticalAlignment** . Por exemplo, se você quiser que um controle seja centralizado horizontalmente e verticalmente, defina **horizontalAlignment** como "Center" e **verticalAlignment** como "Center".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambienteattributes. horizontalAlignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





