---
description: Calcule os vetores tangente, binormal e normal para uma malha.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Função D3DXComputeTangentFrame (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815486"
---
# <a name="d3dxcomputetangentframe-function"></a>Função D3DXComputeTangentFrame

Calcule os vetores tangente, binormal e normal para uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de entrada.

</dd> <dt>

*dwOptions* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores [**D3DXTANGENT**](./d3dxtangent.md) .

Use **NULL** para especificar as seguintes opções:

-   Peso o comprimento normal do vetor pelo ângulo, em radianos, entendeu-se pelas duas bordas deixando o vértice.
-   Calcule coordenadas cartesianas ortogonal das coordenadas de textura UV.
-   As texturas não são encapsuladas nas direções U ou V
-   Derivações parciais em relação às coordenadas de textura são normalizadas.
-   Os vértices são ordenados em uma direção no sentido anti-horário em volta de cada triângulo.
-   Use vetores normais por vértice já presentes na malha de entrada.
-   Os resultados serão armazenados na malha de entrada original. A função falhará se novos vértices precisarem ser criados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função simplesmente chama [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) com os seguintes parâmetros de entrada:


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



As singularidades são tratadas conforme exigido pelo agrupamento de bordas e divisão de vértices. Se qualquer vértice precisar ser dividido, a função falhará. O vetor normal calculado em cada vértice é sempre normalizado para ter comprimento de unidade.

A solução mais robusta para a computação de coordenadas cartesianas ortogonal é não definir sinalizadores D3DXTANGENT \_ ortogonale \_ de \_ você e D3DXTANGENT \_ ortogonalize \_ de \_ V, de forma que as coordenadas ortogonales sejam computadas de ambas as coordenadas de textura UV. No entanto, nesse caso, se U ou V for zero, a função computará coordenadas ortogonal usando D3DXTANGENT \_ ortogonalize \_ de \_ V ou D3DXTANGENT \_ ortogonalize \_ de \_ U, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
