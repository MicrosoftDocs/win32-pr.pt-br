---
description: Função D3DXUVAtlasCriar – Criar um atlas UV para uma malha.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Função D3DXUVAtlasCriar (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31ab8315370b68e2bc71e4a964440e7c7703d392cf5902e244e976080c893779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804077"
---
# <a name="d3dxuvatlascreate-function"></a>Função D3DXUVAtlasCriar

Crie um atlas UV para uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o atlas. No mínimo, a malha deve conter dados de posição e coordenadas de textura 2D.

</dd> <dt>

*dwMaxChartNumber* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número máximo de gráficos para particionar a malha. Consulte comentários sobre os modos de particionamento. Use 0 para dizer ao D3DX que o atlas deve ser parametrizado com base no stretch.

</dd> <dt>

*fMaxStretch* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

A quantidade de alongamento permitida. 0 significa que nenhum alongamento é permitido, 1 significa que qualquer quantidade de alongamento pode ser usada.

</dd> <dt>

*dwWidth* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Largura da textura.

</dd> <dt>

*dwHeight* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Altura da textura.

</dd> <dt>

*fGutter* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

A distância mínima, em texels, entre dois gráficos no atlas. A medianiz sempre é dimensionada pela largura; portanto, se uma medianeira de 2,5 for usada em uma textura 512x512, a distância mínima entre dois gráficos será de 2,5 /512,0 texels.

</dd> <dt>

*dwTextureIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura baseado em zero que identifica qual conjunto de coordenadas de textura usar.

</dd> <dt>

*pdwAdjacency* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Um ponteiro para uma matriz de dados de adjacency. com 3 DWORDs por face, indicando quais triângulos são adjacentes uns aos outros (consulte [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Uma matriz com 3 DWORDS por face. Cada face indica se uma borda é falsa ou não. Uma borda não falsa é indicada por -1, uma borda falsa é indicada por qualquer outro valor. Isso permite a parametrização de uma malha de quads em que as bordas no meio de cada quad não serão cortadas.

</dd> <dt>

*pfIMTArray* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Um ponteiro para uma matriz de tensores de métrica integrados que descreve como alongar um triângulo (consulte [IntegratedMetricTensor](using-uvatlas.md)).

</dd> <dt>

*pCallback* \[ Em\]
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Um ponteiro para uma função de retorno de chamada [(consulte LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que é útil para monitorar o progresso.

</dd> <dt>

*fCallbackFrequency* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifique com que frequência o D3DX chamará o retorno de chamada; um valor padrão razoável é 0,0001f.

</dd> <dt>

*pUserContent* \[ Em\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

</dd> <dt>

*dwOptions* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifique a qualidade dos gráficos gerados. Consulte [**D3DXUVATLAS**](./d3dxuvatlas.md).

</dd> <dt>

*ppMeshOut* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Ponteiro para a malha criada com o atlas (consulte [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*ppFacePartitioning* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Um ponteiro para uma matriz dos dados finais de particionamento facial. Cada elemento contém uma DWORD por face (consulte [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Um ponteiro para uma matriz de vértices remapped. Cada elemento de matriz identifica o vértice original de origem de cada vértice final (se o vértice foi dividido durante o remapeamento). Cada elemento de matriz contém uma DWORD por vértice.

</dd> <dt>

*pfMaxStretchOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Um ponteiro para o valor máximo de alongamento gerado pelo algoritmo atlas. O intervalo está entre 0,0 e 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Um ponteiro para o número de gráficos criados pelo algoritmo atlas. Se dwMaxChartNumber for muito baixo, esse parâmetro retornará o número mínimo de gráficos necessários para criar um atlas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D OK; caso contrário, o valor \_ será D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

D3DXUVAtlasCriar pode particionar geometria de malha de duas maneiras:

-   Com base no número de gráficos
-   Com base no alongamento máximo permitido. Se o stretch máximo permitido for 0, cada triângulo provavelmente estará em seu próprio gráfico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Ferramenta de Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
