---
title: TEXT. disabledFontStyle
description: O atributo disabledFontStyle especifica ou recupera o estilo de fonte usado para o controle de texto quando ele está desabilitado.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- TEXT. disabledFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791285"
---
# <a name="textdisabledfontstyle"></a>TEXT. disabledFontStyle

O atributo **disabledFontStyle** especifica ou recupera o estilo de fonte usado para o controle de texto quando ele está desabilitado.

``` syntax
        elementID.disabledFontStyle
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

Se **disabledFontStyle** não for especificado, **FontStyle** será usado.

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





