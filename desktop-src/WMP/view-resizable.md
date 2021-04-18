---
title: Exibir. redimensionável
description: O atributo redimensionável recupera um valor que indica se a exibição pode ser redimensionada.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- Exibir. redimensionável do Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793876"
---
# <a name="viewresizable"></a>Exibir. redimensionável

O atributo **redimensionável** recupera um valor que indica se a **exibição** pode ser redimensionada.

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** somente leitura com um valor padrão igual ao atributo **TitleBar** .



| Valores | Descrição             |
|--------|-------------------------|
| true   | A exibição pode ser redimensionada.    |
| false  | A exibição não pode ser redimensionada. |



 

## <a name="remarks"></a>Comentários

Se não houver nenhuma **TitleBar** e, portanto, nenhuma janela ou borda, você deverá usar o método **size** para redimensionar o elemento **View** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





