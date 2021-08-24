---
description: 'Método ID3DX10Mesh:: GenerateAdjacencyAndPointReps – gera uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.'
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'Método ID3DX10Mesh:: GenerateAdjacencyAndPointReps (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 55198648be8952f975313dad3019063917eddf4d38f0a7d636039d5802f08e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566936"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>Método ID3DX10Mesh:: GenerateAdjacencyAndPointReps

Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Épsilon* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifica que os vértices que diferem na posição por menos de Épsilon devem ser tratados como coincidentes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Depois que um aplicativo gera informações de adjacência para uma malha, os dados de malha podem ser otimizados para melhorar o desempenho do desenho.

A ordem das entradas no buffer de adjacência é determinada pela ordem dos índices de vértice no buffer de índice. O triângulo adjacente 0 sempre corresponde à borda entre os índices dos cantos 0 e 1. O triângulo adjacente 1 sempre corresponde à borda entre os índices dos cantos 1 e 2, enquanto o triângulo adjacente 2 corresponde à borda entre os índices dos cantos 2 e 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
