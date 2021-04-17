---
title: FontStyle de edição
description: O atributo fontStyle especifica ou recupera o estilo da fonte para o controle caixa de edição.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- Admy. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794484"
---
# <a name="editboxfontstyle"></a>FontStyle de edição

O atributo **FontStyle** especifica ou recupera o estilo da fonte para o controle caixa de edição.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.



| Valor     | Descrição           |
|-----------|-----------------------|
| Negrito      | Estilo de fonte em negrito.      |
| Itálico    | Estilo de fonte em itálico.    |
| Underline | Sublinhar estilo da fonte. |
| Riscado | Estilo da fonte de riscado. |
| Normal    | Estilo de fonte normal.    |



 

## <a name="remarks"></a>Comentários

Qualquer combinação dos valores pode ser usada, separada com espaços. O estilo normal tem prioridade sobre todos os outros valores, e quaisquer outros especificados juntamente com normal serão ignorados.

Para fins de renderização, normal é o estilo de fonte padrão. O valor padrão recuperado desse atributo é "" (cadeia de caracteres vazia).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento admy**](editbox-element.md)
</dt> <dt>

[**FontFace de edição**](editbox-fontface.md)
</dt> <dt>

[**Mythe. fontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





