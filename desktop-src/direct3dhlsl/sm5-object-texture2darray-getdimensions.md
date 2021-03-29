---
title: 'Função Texture2DArray:: GetDimensions'
description: 'Retorna as dimensões do recurso. | Função Texture2DArray:: GetDimensions'
ms.assetid: 0f6d88b3-195d-4f8c-ac31-ac90129a233e
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
ms.openlocfilehash: b3a78bd12f6924c85d4d395c3cdf73443ae51478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968280"
---
# <a name="texture2darraygetdimensions-function"></a>Função Texture2DArray:: GetDimensions

Retorna as dimensões do recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
void GetDimensions(
  in  UINT MipLevel,
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MipLevel* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Opcional. O nível de mipmap (deve ser especificado se *NumberOfLevels* for usado).

</dd> <dt>

*Largura* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

A largura do recurso, em texels.

</dd> <dt>

*Altura* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

A altura do recurso, em texels.

</dd> <dt>

*Elementos* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de elementos na matriz.

</dd> <dt>

*NumberOfLevels* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O número de níveis de mipmap (também requer *MipLevel* ).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Nothing

## <a name="remarks"></a>Comentários

Esta é uma lista das versões sobrecarregadas desse método.


```
void GetDimensions(UINT MipLevel, 
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfLevels);

void GetDimensions (out UINT Width,
  out float Height,
  out float Elements);

void GetDimensions(UINT MipLevel,
  out float Width,
  out float Height,
  out float Elements,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
