---
title: Função Texture3D::GetDimensions
description: Retorna as dimensões do recurso. | Função Texture3D::GetDimensions
ms.assetid: 4a08f14f-7489-4ed1-bf94-4f63f1002eab
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
ms.openlocfilehash: 8a7dd6248b7b6effc08e510ea56da6426c41dc54418bf7ee5da8cdc3c9ad965a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985706"
---
# <a name="texture3dgetdimensions-function"></a>Função Texture3D::GetDimensions

Retorna as dimensões do recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MipLevel* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Opcional. Nível de Mipmap (deve ser especificado se *NumberOfLevels* for usado).

</dd> <dt>

*Largura* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

A largura do recurso, em texels.

</dd> <dt>

*Altura* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

A altura do recurso, em texels.

</dd> <dt>

*Profundidade* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

A profundidade do recurso, em texels.

</dd> <dt>

*NumberOfLevels* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O número de níveis de mipmap (requer *também MipLevel).*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nada

## <a name="remarks"></a>Comentários

Esta é uma lista das versões sobrecarregadas desse método.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Depth,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Depth);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Depth,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Depth);
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
