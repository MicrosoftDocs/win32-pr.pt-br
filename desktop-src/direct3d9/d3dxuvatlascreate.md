---
description: Função D3DXUVAtlasCreate – criar um Atlas UV para uma malha.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Função D3DXUVAtlasCreate (D3DX9Mesh. h)
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
ms.openlocfilehash: 5f382e7d59f3a5b5db8ba3cfd65ba6cc1a11e86d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117824"
---
# <a name="d3dxuvatlascreate-function"></a>Função D3DXUVAtlasCreate

Crie um Atlas UV para uma malha.

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

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o Atlas. No mínimo, a malha deve conter dados de posição e coordenadas de textura 2D.

</dd> <dt>

*dwMaxChartNumber* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número máximo de gráficos para particionar a malha. Consulte comentários sobre os modos de particionamento. Use 0 para informar ao D3DX que o Atlas deve ser parametrizado com base na ampliação.

</dd> <dt>

*fMaxStretch* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

A quantidade de alongamento permitida. 0 significa que nenhum alongamento é permitido, 1 significa que qualquer quantidade de alongamento pode ser usada.

</dd> <dt>

*dwWidth* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Largura da textura.

</dd> <dt>

*dwHeight* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altura da textura.

</dd> <dt>

*fGutter* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

A distância mínima, em texels, entre dois gráficos no Atlas. A medianiz sempre é dimensionada pela largura; Portanto, se uma medianiz de 2,5 for usada em uma textura 512x512, a distância mínima entre dois gráficos será 2,5/512,0 texels.

</dd> <dt>

*dwTextureIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.

</dd> <dt>

*pdwAdjacency* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Um ponteiro para uma matriz de dados de adjacência. com 3 DWORDs por face, indicando quais triângulos são adjacentes entre si (consulte [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Uma matriz com 3 DWORDs por face. Cada face indica se uma borda é falsa ou não. Uma borda diferente de falsa é indicada por-1, uma borda falsa é indicada por qualquer outro valor. Isso permite a parametrização de uma malha de quatro processadores em que as bordas no meio do meio de cada Quad não serão recortadas.

</dd> <dt>

*pfIMTArray* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Um ponteiro para uma matriz de tempos de métricas integrados que descreve como alongar um triângulo (consulte [IntegratedMetricTensor](using-uvatlas.md)).

</dd> <dt>

*pCallback* \[ no\]
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Um ponteiro para uma função de retorno de chamada (consulte [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que é útil para monitorar o progresso.

</dd> <dt>

*fCallbackFrequency* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifique com que frequência o D3DX chamará o retorno de chamada; um valor padrão razoável é 0,0001 f.

</dd> <dt>

*pUserContent* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada; normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

</dd> <dt>

*dwOptions* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifique a qualidade dos gráficos gerados. Consulte [**D3DXUVATLAS**](./d3dxuvatlas.md).

</dd> <dt>

*ppMeshOut* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Ponteiro para a malha criada com o Atlas (consulte [**ID3DXMesh**](id3dxmesh.md)).

</dd> <dt>

*ppFacePartitioning* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Um ponteiro para uma matriz dos dados de particionamento de face final. Cada elemento contém um DWORD por face (consulte [**ID3DXBuffer**](id3dxbuffer.md)).

</dd> <dt>

*ppVertexRemapArray* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Um ponteiro para uma matriz de vértices remapeados. Cada elemento da matriz identifica o vértice original do qual cada vértice final veio (se o vértice foi dividido durante o remapeamento). Cada elemento de matriz contém um DWORD por vértice.

</dd> <dt>

*pfMaxStretchOut* \[ fora\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Um ponteiro para o valor máximo de Stretch gerado pelo algoritmo do Atlas. O intervalo está entre 0,0 e 1,0.

</dd> <dt>

*pdwNumChartsOut* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Um ponteiro para o número de gráficos criados pelo algoritmo do Atlas. Se dwMaxChartNumber for muito baixo, esse parâmetro retornará o número mínimo de gráficos necessários para criar um Atlas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

D3DXUVAtlasCreate pode particionar a geometria de malha de duas maneiras:

-   Com base no número de gráficos
-   Com base na ampliação máxima permitida. Se a ampliação máxima permitida for 0, cada triângulo provavelmente estará em seu próprio gráfico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Ferramenta de Command-Line do Atlas de UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
