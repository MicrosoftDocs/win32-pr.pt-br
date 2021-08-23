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
ms.openlocfilehash: 81c768d138f6ee1853f9930a56f1a1864b468e8be9ff421f4dba1698b790053c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986026"
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

## <a name="return-value"></a>Valor retornado

Tipo: **T**

O *n*<sup>º</sup> do ponto de controle.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




