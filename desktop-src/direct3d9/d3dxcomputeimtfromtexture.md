---
description: Calcula o IMT por triângulo de uma textura mapeada em uma malha, a ser usada opcionalmente como entrada para as funções UVAtlas do D3DX.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Função D3DXComputeIMTFromTexture (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012146"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>Função D3DXComputeIMTFromTexture

Calcula o IMT por triângulo de uma textura mapeada em uma malha, a ser usada opcionalmente como entrada para as [funções UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)do D3DX.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Um ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o IMT.

</dd> <dt>

*pTexture* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Um ponteiro para a textura (consulte [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) que é mapeado para a malha.

</dd> <dt>

*dwTextureIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.

</dd> <dt>

*dwOptions* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opções de quebra automática de textura. Essa é uma combinação de um ou mais [**sinalizadores D3DXIMT**](./d3dximt-flags.md).

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

Dada uma textura que mapeia sobre a superfície da malha, o algoritmo computa o IMT para cada face. Isso fará com que os triângulos que contêm dados de sinal de baixa frequência contenham menos espaço no Atlas de textura final quando parametrizados com as funções UVAtlas. Pressupõe-se que a textura seja interpolada na malha bilinearmente.

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

 

 
