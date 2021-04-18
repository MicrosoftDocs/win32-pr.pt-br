---
description: Executa cálculos de quadro tangente em uma malha. Os vetores tangente, binormal e opcionalmente normais são gerados. As singularidades são tratadas conforme exigido pelo agrupamento de bordas e divisão de vértices.
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: Função D3DXComputeTangentFrameEx (D3DX9Mesh. h)
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
ms.openlocfilehash: 58c7e8a1f1f7247d6a3ecc92d5771d68c9c3e5a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815526"
---
# <a name="d3dxcomputetangentframeex-function"></a>Função D3DXComputeTangentFrameEx

Executa cálculos de quadro tangente em uma malha. Os vetores tangente, binormal e opcionalmente normais são gerados. As singularidades são tratadas conforme exigido pelo agrupamento de bordas e divisão de vértices.

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

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***

Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de entrada.

</dd> <dt>

*dwTextureInSemantic* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica a semântica de entrada da coordenada de textura. Se D3DX \_ padrão, a função assumirá que não há coordenadas de textura e a função falhará, a menos que o cálculo de vetor normal seja especificado.

</dd> <dt>

*dwTextureInIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Se uma malha tiver várias coordenadas de textura, especificará a coordenada de textura a ser usada para os cálculos de quadro tangente. Se for zero, a malha terá apenas uma única coordenada de textura.

</dd> <dt>

*dwUPartialOutSemantic* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica a semântica de saída para o tipo, normalmente D3DDECLUSAGE \_ tangente, que descreve onde o derivativo parcial em relação à coordenada de textura U será armazenado. Se D3DX \_ padrão, esse derivativo parcial não será armazenado.

</dd> <dt>

*dwUPartialOutIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o índice semântico no qual armazenar o derivativo parcial em relação à coordenada de textura de U.

</dd> <dt>

*dwVPartialOutSemantic* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o tipo [**D3DDECLUSAGE**](./d3ddeclusage.md) , geralmente D3DDECLUSAGE \_ binormal, que descreve onde o derivativo parcial em relação à coordenada de textura V será armazenado. Se D3DX \_ padrão, esse derivativo parcial não será armazenado.

</dd> <dt>

*dwVPartialOutIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o índice semântico no qual armazenar o derivativo parcial em relação à coordenada de textura V.

</dd> <dt>

*dwNormalOutSemantic* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica a semântica normal de saída, normalmente D3DDECLUSAGE \_ normal, que descreve onde o vetor normal em cada vértice será armazenado. Se D3DX \_ padrão, esse vetor normal não será armazenado.

</dd> <dt>

*dwNormalOutIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o índice semântico no qual armazenar o vetor normal em cada vértice.

</dd> <dt>

*dwOptions* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores [**D3DXTANGENT**](./d3dxtangent.md) que especificam opções de computação de quadro tangente. Se for **NULL**, as seguintes opções serão especificadas:



| Description                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) Valor do sinalizador                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| Peso o comprimento normal do vetor pelo ângulo, em radianos, entendeu-se pelas duas bordas deixando o vértice. | &! (D3DXTANGENT \_ PESO \_ pelo \_ peso de D3DXTANGENT de área \| \_ igual a \_ )                |
| Calcular coordenadas cartesianas ortogonal de coordenadas de textura (u, v). Consulte Observações.                   | &! (D3DXTANGENT \_ ORTOGONALize \_ de \_ U \| D3DXTANGENT \_ ortogonalize \_ da \_ V) |
| As texturas não são encapsuladas nas direções u ou v                                                     | &! (D3DXTANGENT \_ CODIFICAÇÃO \_ UV)                                                      |
| Derivações parciais em relação às coordenadas de textura são normalizadas.                                  | &! (D3DXTANGENT \_ Não \_ normalizar \_ parciais)                                     |
| Os vértices são ordenados em uma direção no sentido anti-horário em volta de cada triângulo.                               | &! (D3DXTANGENT \_ PV de vento \_ )                                                      |
| Use vetores normais por vértice já presentes na malha de entrada.                                         | &! (D3DXTANGENT \_ CALCULAR \_ Normals)                                            |



 

Se \_ a geração \_ de D3DXTANGENT no \_ local não for definida, a malha de entrada será clonada. Portanto, a malha original deve ter espaço suficiente para armazenar o vetor normal calculado e os dados derivados parciais.

</dd> <dt>

*pdwAdjacency* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha. O número de bytes nessa matriz deve ser pelo menos 3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> <dt>

*fPartialEdgeThreshold* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifica o cosseno máximo do ângulo no qual dois derivativos parciais são considerados incompatíveis entre si. Se o produto de ponto da direção dos dois derivativos parciais em triângulos adjacentes for menor ou igual a esse limite, os vértices compartilhados entre esses triângulos serão divididos.

</dd> <dt>

*fSingularPointThreshold* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifica a magnitude máxima de um derivativo parcial no qual um vértice será considerado singular. Como vários triângulos são incidentes em um ponto que têm quadros tangentes próximos, mas completamente cancelam um ao outro (como na parte superior de uma esfera), a magnitude do derivativo parcial diminuirá. Se a magnitude for menor ou igual a esse limite, o vértice será dividido para cada triângulo que o contém.

</dd> <dt>

*fNormalEdgeThreshold* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Semelhante a fPartialEdgeThreshold, especifica o cosseno máximo do ângulo entre dois normais que é um limite além do qual os vértices compartilhados entre triângulos serão divididos. Se o produto de ponto de dois normais for menor que o limite, os vértices compartilhados serão divididos, formando uma borda rígida entre triângulos vizinhos. Se o produto de ponto for maior que o limite, os triângulos vizinhos terão seus normais interpolados.

</dd> <dt>

*ppMeshOut* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\*\***

Endereço de um ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de saída que recebe os dados de vetor calculados tangente, binormal e normal.

</dd> <dt>

*ppVertexMapping* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

Endereço de um ponteiro para um objeto de buffer [**ID3DXBuffer**](id3dxbuffer.md) de saída que recebe um mapeamento de novos vértices computados por esse método para os vértices originais. O buffer é uma matriz de DWORDs, com o tamanho da matriz definido como o número de vértices em ppMeshOut.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Uma versão simplificada dessa função está disponível como [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md).

O vetor normal calculado em cada vértice é sempre normalizado para ter comprimento de unidade.

A solução mais robusta para a computação de coordenadas cartesianas ortogonal é não definir sinalizadores D3DXTANGENT \_ ortogonale \_ de \_ você e D3DXTANGENT \_ ortogonalize \_ de \_ V, de forma que as coordenadas ortogonales sejam computadas de ambas as coordenadas de textura que você e V. No entanto, nesse caso, se u ou v for zero, a função computará coordenadas ortogonal usando D3DXTANGENT \_ ortogonalize \_ de \_ v ou D3DXTANGENT \_ ortogonalize \_ de \_ u, respectivamente.

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

 

 
