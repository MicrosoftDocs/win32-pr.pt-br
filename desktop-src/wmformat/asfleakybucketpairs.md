---
title: ASFLeakyBucketPairs
description: O atributo ASFLeakyBucketPairs é um atributo opcional que descreve os requisitos de buffer para um arquivo de taxa de bits variável.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- Formato de mídia do Windows ASFLeakyBucketPairs
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76de649a069b0cfec74fabe1a41d6cfa659b39448257a4bc966065e1bce98ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434615"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

O **atributo ASFLeakyBucketPairs** é um atributo opcional que descreve os requisitos de buffer para um arquivo de taxa de bits variável.

## <a name="global-constant"></a>Constante global

g \_ wszASFLeakyBucketPairs

## <a name="data-type"></a>Tipo de Dados

**TIPO WMT \_ \_ BINARY**

## <a name="remarks"></a>Comentários

Esse atributo tem o seguinte formato:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Em *que wReserved* deve ser igual a zero e *bucket* é uma matriz de estruturas [**WM \_ LEAKY BUCKET \_ \_ PAIR.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) A matriz deve conter pelo menos duas entradas, mas pode ser maior. O objeto de leitor usa esse atributo para determinar a quantidade de conteúdo a ser armazenado em buffer antes da reprodução.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




