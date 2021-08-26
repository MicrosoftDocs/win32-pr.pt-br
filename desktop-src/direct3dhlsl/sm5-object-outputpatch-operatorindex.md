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
ms.openlocfilehash: 684925491ce7b5ac50cb293b3c8a0270557c9b9e65fcfcde63e9699127bc7ed0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023466"
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

## <a name="return-value"></a>Valor retornado

Tipo: **T**

O *n*<sup>º</sup> do ponto de controle.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




