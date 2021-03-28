---
title: 'Função Texture2D:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture2D:: GetDimensions'
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
keywords:
- Função GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989220"
---
# <a name="texture2dgetdimensions-function"></a>Função Texture2D:: GetDimensions

Retorna as dimensões do recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MipLevel* \[ no\]
</dt> <dd>

Tipo: **uint**

Opcional. O nível de mipmap (deve ser especificado se *NumberOfLevels* for usado).

</dd> <dt>

*Largura* \[ fora\]
</dt> <dd>

Tipo: **uint**

A largura do recurso, em texels.

</dd> <dt>

*Altura* \[ fora\]
</dt> <dd>

Tipo: **uint**

A altura do recurso, em texels.

</dd> <dt>

*NumberOfLevels* \[ fora\]
</dt> <dd>

Tipo: **uint**

O número de níveis de mipmap (também requer *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nothing

## <a name="remarks"></a>Comentários

Esta é uma lista das versões sobrecarregadas desse método.


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




