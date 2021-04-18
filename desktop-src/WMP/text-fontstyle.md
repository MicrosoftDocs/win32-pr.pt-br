---
title: TEXT. fontStyle
description: O atributo fontStyle especifica ou recupera o estilo da fonte para o controle de texto.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751933"
---
# <a name="textfontstyle"></a>TEXT. fontStyle

O atributo **FontStyle** especifica ou recupera o estilo da fonte para o controle de texto.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.



| Valor     | Descrição                 |
|-----------|-----------------------------|
| Negrito      | Estilo de fonte em negrito.            |
| Itálico    | Estilo de fonte em itálico.          |
| Underline | Sublinhar estilo da fonte.       |
| Riscado | Estilo da fonte de riscado.       |
| Normal    | Padrão. Estilo de fonte normal. |



 

## <a name="remarks"></a>Comentários

Qualquer combinação dos valores pode ser usada, separada com espaços. O estilo normal tem prioridade sobre todos os outros valores, e quaisquer outros especificados juntamente com normal serão ignorados.

Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento de texto**](text-element.md)
</dt> </dl>

 

 





