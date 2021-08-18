---
description: Compactar dados de particionamento de malha em um Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Função D3DXUVAtlasPack (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6990d6fbc114c874b31d0035a2415d48161d3065718efce3783a041a2097e96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749656"
---
# <a name="d3dxuvatlaspack-function"></a>Função D3DXUVAtlasPack

Compactar dados de particionamento de malha em um Atlas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o Atlas. No mínimo, a malha deve conter dados de posição e coordenadas de textura 2D.

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

*pdwPartitionResultAdjacency* 
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha. Ele deve ser derivado do ppPartitionResultAdjacency retornado de [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md). Esse valor não pode ser **nulo**, pois o pacote precisa saber onde os gráficos foram cortados na etapa de partição para localizar as bordas de cada gráfico.

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

Um ponteiro void a ser passado de volta para a função de retorno de chamada.

</dd> <dt>

*dwOptions* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Este parâmetro de opções está reservado no momento.

</dd> <dt>

*pFacePartitioning* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Um ponteiro para um [**ID3DXBuffer**](id3dxbuffer.md) que contém a matriz do particionamento de face final. Cada elemento contém um DWORD por face.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
