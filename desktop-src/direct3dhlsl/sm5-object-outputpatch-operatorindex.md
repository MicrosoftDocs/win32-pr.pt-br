---
title: 'Função OutputPatch:: Operator'
description: 'Retorna o enésimo ponto de controle no patch. | Função OutputPatch:: Operator'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298191"
---
# <a name="outputpatchoperator--function"></a>Função OutputPatch:: Operator

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
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




