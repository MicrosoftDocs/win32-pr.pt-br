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
ms.openlocfilehash: c655313147a568e5eb33ddf30a2acd2be3549ca4d57bc8510ef974199ea3740d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985866"
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

## <a name="return-value"></a>Valor retornado

Nada

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



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
