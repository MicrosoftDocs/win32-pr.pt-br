---
title: LISTBOX. fontStyle
description: O atributo fontStyle especifica ou recupera o estilo da fonte para o controle da caixa de listagem.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- Windows Media Player LISTBOX. fontStyle
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258064ca4ee97fc33bb98bf64d8e3dcf305c5d7e045282a5218a060e904aff50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575033"
---
# <a name="listboxfontstyle"></a>LISTBOX. fontStyle

O atributo **FontStyle** especifica ou recupera o estilo da fonte para o controle da caixa de listagem.

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

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**Caixa de listagem. fontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





