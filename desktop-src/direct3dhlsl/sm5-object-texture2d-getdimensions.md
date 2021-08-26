---
title: Função Texture2D::GetDimensions
description: Retorna as dimensões do recurso. | Função Texture2D::GetDimensions
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
ms.openlocfilehash: 46eb5101dc119d2779f60d2e2b39a42c695933a5bffd477b407fea56c930038c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067696"
---
# <a name="texture2dgetdimensions-function"></a>Função Texture2D::GetDimensions

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

*MipLevel* \[ Em\]
</dt> <dd>

Tipo: **uint**

Opcional. O nível de mipmap (deve ser especificado se *NumberOfLevels* for usado).

</dd> <dt>

*Largura* \[ out\]
</dt> <dd>

Tipo: **uint**

A largura do recurso, em texels.

</dd> <dt>

*Altura* \[ out\]
</dt> <dd>

Tipo: **uint**

A altura do recurso, em texels.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Tipo: **uint**

O número de níveis de mipmap (requer *também MipLevel).*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nada

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



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




