---
title: TEXT.hoverFontStyle
description: O atributo hoverFontStyle especifica ou recupera o estilo de fonte usado para o controle Texto quando o cursor do mouse sobre ele.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- TEXT.hoverFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04f2ae8e4231ca89f37a65e591271f2536679da649d1efd22ffc1063c89d17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134619"
---
# <a name="texthoverfontstyle"></a>TEXT.hoverFontStyle

O **atributo hoverFontStyle** especifica ou recupera o estilo de fonte usado para o controle Texto quando o cursor do mouse sobre ele.

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma Cadeia de **caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.



| Valor     | Descrição           |
|-----------|-----------------------|
| Negrito      | Estilo de fonte em negrito.      |
| Itálico    | Estilo de fonte itálico.    |
| Underline | Estilo de fonte sublinhado. |
| Riscado | Estilo de fonte de ataque. |
| Normal    | Estilo de fonte normal.    |



 

## <a name="remarks"></a>Comentários

Qualquer combinação dos valores pode ser usada, separada por espaços. O estilo Normal tem prioridade sobre todos os outros valores e quaisquer outros especificados junto com Normal serão ignorados.

Se **hoverFontStyle** não for especificado, **fontStyle** será usado.

Consulte o [atributo value](text-value.md) para um exemplo que ilustra como os atributos do **elemento TEXT** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





