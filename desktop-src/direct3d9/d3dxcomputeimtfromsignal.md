---
description: Calcula o IMT por triângulo de um sinal especificado pelo aplicativo personalizado que varia na superfície da malha (geralmente com uma frequência maior do que os dados de vértice). O sinal é avaliado por meio de uma função de retorno de chamada especificada pelo usuário.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: Função D3DXComputeIMTFromSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765028"
---
# <a name="d3dxcomputeimtfromsignal-function"></a>Função D3DXComputeIMTFromSignal

Calcula o IMT por triângulo de um sinal especificado pelo aplicativo personalizado que varia na superfície da malha (geralmente com uma frequência maior do que os dados de vértice). O sinal é avaliado por meio de uma função de retorno de chamada especificada pelo usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Um ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o IMT.

</dd> <dt>

*dwTextureIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.

</dd> <dt>

*uSignalDimension* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de componentes em cada ponto de dados no sinal.

</dd> <dt>

*fMaxUVDistance* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

A distância máxima entre os vértices; o algoritmo continua subdividindo até que a distância entre todos os vértices seja menor ou igual a fMaxUVDistance.

</dd> <dt>

*dwOptions* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opções de quebra automática de textura. Essa é uma combinação de um ou mais [**sinalizadores D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pSignalCallback* \[ no\]
</dt> <dd>

Tipo: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**

Um ponteiro para uma função de avaliador fornecida pelo usuário, que será usado para calcular o valor de sinal em coordenadas U, x arbitrárias. A função segue o protótipo de [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).

</dd> <dt>

*pUserData* \[ no\]
</dt> <dd>

Tipo: **void \***

Um ponteiro para um valor definido pelo usuário que é passado para a função de retorno de chamada de sinal. Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Um ponteiro para uma função de retorno de chamada para monitorar o progresso da computação IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Um ponteiro para uma variável definida pelo usuário que é passada para a função de retorno de chamada de status. Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.

</dd> <dt>

*ppIMTData* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Um ponteiro para o buffer (consulte [**ID3DXBuffer**](id3dxbuffer.md)) que contém a matriz IMT retornada. Essa matriz pode ser fornecida como entrada para as [funções D3DX UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) para priorizar a alocação de espaço de textura na parametrização de textura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Essa função requer que a malha de entrada contenha um mapeamento de textura de sinal para malha (as coordenadas de IE. Texture). Ele permite que o usuário defina um sinal arbitrariamente sobre a superfície da malha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Usando o UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
