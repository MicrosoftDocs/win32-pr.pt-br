---
title: TEXT.fontStyle
description: O atributo fontStyle especifica ou recupera o estilo da fonte para o controle Text.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT.fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fbdbe021890b3a76fbae3838cbebe958956af82ff468f990fe6fd9e91345a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762896"
---
# <a name="textfontstyle"></a>TEXT.fontStyle

O **atributo fontStyle** especifica ou recupera o estilo da fonte para o controle Text.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma Cadeia de **caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.



| Valor     | Descrição                 |
|-----------|-----------------------------|
| Negrito      | Estilo de fonte em negrito.            |
| Itálico    | Estilo de fonte itálico.          |
| Underline | Estilo de fonte sublinhado.       |
| Riscado | Estilo de fonte de ataque.       |
| Normal    | Padrão. Estilo de fonte normal. |



 

## <a name="remarks"></a>Comentários

Qualquer combinação dos valores pode ser usada, separada por espaços. O estilo Normal tem prioridade sobre todos os outros valores e quaisquer outros especificados junto com Normal serão ignorados.

Consulte o [atributo value](text-value.md) para um exemplo que ilustra como os atributos do **elemento TEXT** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





