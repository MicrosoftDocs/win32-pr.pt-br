---
title: 'Função RWTexture1D:: Operator'
description: 'Retorna uma variável de recurso. | Função RWTexture1D:: Operator'
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
keywords:
- Função Operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506381"
---
# <a name="rwtexture1doperator--function"></a>Função RWTexture1D:: Operator

Retorna uma variável de recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ no\]
</dt> <dd>

Tipo: **uint**

A posição do índice. Contém a coordenada x.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **R**

Uma variável de recurso.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWTexture1D](sm5-object-rwtexture1d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




