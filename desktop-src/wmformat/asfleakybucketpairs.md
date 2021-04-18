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
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105797576"
---
# <a name="asfleakybucketpairs"></a>ASFLeakyBucketPairs

O atributo **ASFLeakyBucketPairs** é um atributo opcional que descreve os requisitos de buffer para um arquivo de taxa de bits variável.

## <a name="global-constant"></a>Constante global

g \_ wszASFLeakyBucketPairs

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ binário**

## <a name="remarks"></a>Comentários

Esse atributo tem o seguinte formato:

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

Em que *wReserved* deve ser igual a zero e *Bucket* é uma matriz de estruturas de [**\_ \_ \_ pares de buckets de vazamento do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) . A matriz deve conter pelo menos duas entradas, mas pode ser maior. O objeto leitor usa esse atributo para determinar a quantidade de conteúdo a ser armazenada em buffer antes da reprodução.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




