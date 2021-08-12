---
description: Calcule IMTs por triângulo de dados por vértice. Essa função permite que você calcule a IMT com base em qualquer valor em uma malha (cor, normal etc.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Função D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41d635bf436e139e4c44db75b1057cebc3a50cfee114a35bfc75a9de84abc404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299453"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>Função D3DXComputeIMTFromPerVertexSignal

Calcule IMTs por triângulo de dados por vértice. Essa função permite que você calcule a IMT com base em qualquer valor em uma malha (cor, normal etc.).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Um ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular a IMT.

</dd> <dt>

*pfVertexSignal* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Um ponteiro para uma matriz de dados por vértice da qual a IMT será computada. O tamanho da matriz é uSignalStride v, em que v é o número de \* vtices na malha.

</dd> <dt>

*uSignalDimension* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de floats por vértice.

</dd> <dt>

*uSignalStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de bytes por vértice na matriz. Isso deve ser um múltiplo de sizeof(float)

</dd> <dt>

*dwOptions* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opções de quebra de textura. Essa é uma combinação de um ou mais [**SINALIZADORES D3DXIMT.**](./d3dximt-flags.md)

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Um ponteiro para uma função de retorno de chamada para monitorar o progresso da computação de IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Um ponteiro para uma variável definida pelo usuário que é passada para a função de retorno de chamada de status. Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

</dd> <dt>

*ppIMTData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Um ponteiro para o buffer (consulte [**ID3DXBuffer**](id3dxbuffer.md)) que contém a matriz IMT retornada. Essa matriz pode ser fornecida como entrada para as funções [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) D3DX para priorizar a alocação de espaço de textura na parametrização de textura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D OK; caso contrário, o valor \_ será D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Usando UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
