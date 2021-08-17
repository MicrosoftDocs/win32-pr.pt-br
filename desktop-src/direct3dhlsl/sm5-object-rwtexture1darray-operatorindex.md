---
title: Função RWTexture1DArray::Operator
description: Retorna uma variável de recurso. | Função RWTexture1DArray::Operator
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
keywords:
- Função de operador HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e0735e3d9945d15c2f8473155612a40cbf652349eb531f089f5a4aa44451484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509278"
---
# <a name="rwtexture1darrayoperator--function"></a>Função RWTexture1DArray::Operator

Retorna uma variável de recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ Em\]
</dt> <dd>

Tipo: **uint2**

A posição do índice. O primeiro componente contém a coordenada x. O segundo componente indica a fatia de matriz desejada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




