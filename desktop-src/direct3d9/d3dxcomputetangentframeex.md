---
description: Executa cálculos de quadros tangentes em uma malha. Vetores tangentes, binormais e, opcionalmente, normais são gerados. As singularidades são tratadas conforme necessário agrupando bordas e dividindo vértices.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Função D3DXComputeTangentFrameEx (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d091b7ca243e4833cd6aa36a409fca32069e52a267ec3f588b338777ed34338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988666"
---
# <a name="d3dxcomputetangentframeex-function"></a>Função D3DXComputeTangentFrameEx

Executa cálculos de quadros tangentes em uma malha. Vetores tangentes, binormais e, opcionalmente, normais são gerados. As singularidades são tratadas conforme necessário agrupando bordas e dividindo vértices.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Ponteiro para um objeto [**de malha ID3DXMesh**](id3dxmesh.md) de entrada.

</dd> <dt>

*dwTextureInSemantic* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica a semântica de entrada da coordenada de textura. Se D3DX DEFAULT, a função assumirá que não há coordenadas de textura e a função falhará, a menos que o cálculo de vetor \_ normal seja especificado.

</dd> <dt>

*dwTextureInIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se uma malha tiver várias coordenadas de textura, especificará a coordenada de textura a ser usada para os cálculos de quadro tangente. Se zero, a malha terá apenas uma única coordenada de textura.

</dd> <dt>

*dwUPartialOutSemantic* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica a semântica de saída para o tipo, normalmente D3DDECLUSAGE TANGENT, que descreve onde o derivado parcial em relação à coordenada \_ de textura U será armazenado. Se D3DX \_ DEFAULT, esse derivado parcial não será armazenado.

</dd> <dt>

*dwUPartialOutIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o índice semântico no qual armazenar a derivada parcial em relação à coordenada de textura U.

</dd> <dt>

*dwVPartialOutSemantic* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o tipo [**D3DDECLUSAGE,**](./d3ddeclusage.md) normalmente D3DDECLUSAGE BINORMAL, que descreve onde o derivado parcial em relação à coordenada de \_ textura V será armazenado. Se D3DX \_ DEFAULT, esse derivado parcial não será armazenado.

</dd> <dt>

*dwVPartialOutIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o índice semântico no qual armazenar o derivado parcial em relação à coordenada de textura V.

</dd> <dt>

*dwNormalOutSemantic* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica a semântica normal de saída, normalmente D3DDECLUSAGE NORMAL, que descreve onde o vetor normal em \_ cada vértice será armazenado. Se D3DX \_ DEFAULT, esse vetor normal não será armazenado.

</dd> <dt>

*dwNormalOutIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o índice semântico no qual armazenar o vetor normal em cada vértice.

</dd> <dt>

*dwOptions* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais [**sinalizadores D3DXTANGENT**](./d3dxtangent.md) que especificam opções de computação de quadro tangente. Se **NULL**, as seguintes opções serão especificadas:



| Descrição                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Valor do sinalizador                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Peso do comprimento do vetor normal pelo ângulo, em radianos, subtendido pelas duas bordas que deixam o vértice. | &! ( D3DXTANGENT \_ PESO \_ POR \_ ÁREA \| D3DXTANGENT \_ PESO IGUAL A \_ )                |
| Computar coordenadas cartesianas ortogonais de coordenadas de textura (u, v). Consulte Observações.                   | &! ( D3DXTANGENT \_ ORTOGONALIZE \_ DE \_ U \| D3DXTANGENT \_ ORTOGONALIZE \_ DE V \_ ) |
| As texturas não são envolvidas em direções u ou v                                                     | &! ( D3DXTANGENT \_ WRAP \_ UV )                                                      |
| Derivados parciais em relação às coordenadas de textura são normalizados.                                  | &! ( D3DXTANGENT \_ NÃO \_ NORMALIZAR \_ PARCIAIS )                                     |
| Os vértices são ordenados em uma direção anti-horário em torno de cada triângulo.                               | &! ( D3DXTANGENT \_ WIND \_ CW )                                                      |
| Use vetores normais por vértice já presentes na malha de entrada.                                         | &! ( D3DXTANGENT \_ CALCULATE \_ NORMALS )                                            |



 

Se D3DXTANGENT GENERATE IN PLACE não estiver definido, a malha \_ de entrada será \_ \_ clonada. Portanto, a malha original deve ter espaço suficiente para armazenar o vetor normal calculado e os dados derivados parciais.

</dd> <dt>

*pdwAdjacency* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha. O número de bytes nessa matriz deve ser pelo menos 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).

</dd> <dt>

*fPartialEdgeThreshold* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifica o cosseno máximo do ângulo no qual dois derivados parciais são considerados incompatíveis entre si. Se o produto de ponto da direção dos dois derivados parciais em triângulos adjacentes for menor ou igual a esse limite, os vértices compartilhados entre esses triângulos serão divididos.

</dd> <dt>

*fSingularPointThreshold* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifica a magnitude máxima de um derivado parcial no qual um vértice será considerado singular. Como vários triângulos são incidentes em um ponto que têm quadros tangentes próximos, mas cancelam completamente uns aos outros (como na parte superior de uma esfera), a magnitude do derivado parcial diminuirá. Se a magnitude for menor ou igual a esse limite, o vértice será dividido para cada triângulo que o contém.

</dd> <dt>

*fNormalEdgeThreshold* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Semelhante a fPartialEdgeThreshold, especifica o cosseno máximo do ângulo entre dois normais que é um limite além do qual os vértices compartilhados entre triângulos serão divididos. Se o produto de ponto dos dois normais for menor que o limite, os vértices compartilhados serão divididos, formar uma borda dura entre triângulos vizinhos. Se o produto de ponto for maior que o limite, os triângulos vizinhos terão seus normais interpolados.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Endereço de um ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de saída que recebe os dados de vetor normal, binormal e tangente computados.

</dd> <dt>

*ppVertexMapping* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Endereço de um ponteiro para um objeto de buffer [**ID3DXBuffer**](id3dxbuffer.md) de saída que recebe um mapeamento de novos vértices computados por esse método para os vértices originais. O buffer é uma matriz de DWORDs, com o tamanho da matriz definido como o número de vértices em ppMeshOut.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Uma versão simplificada dessa função está disponível como [**D3DXComputeTangentFrame.**](d3dxcomputetangentframe.md)

O vetor normal calculado em cada vértice é sempre normalizado para ter comprimento de unidade.

A solução mais robusta para calcular coordenadas ortogonais cartesianas é não definir sinalizadores D3DXTANGENT \_ ORTHOGONALIZE DE você e \_ \_ D3DXTANGENT \_ ORTHOGONALIZE FROM V, de modo que as \_ \_ coordenadas ortogonais sejam calculadas de ambas as coordenadas de textura, você e v. No entanto, nesse caso, se u ou v for zero, a função calculará coordenadas ortogonais usando D3DXTANGENT \_ ORTHOGONALIZE FROM V ou \_ \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
