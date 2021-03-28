---
title: 'Função InputPatch:: Operator'
description: 'Retorna o enésimo ponto de controle no patch. | Função InputPatch:: Operator'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172706"
---
# <a name="inputpatchoperator--function"></a>Função InputPatch:: Operator

Retorna o *n*<sup>º</sup> do ponto de controle no patch.

## <a name="syntax"></a>Sintaxe

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **uint**

O índice de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **T**

O *n*<sup>º</sup> do ponto de controle.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




