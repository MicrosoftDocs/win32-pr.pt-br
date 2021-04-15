---
description: Cria um objeto ID3DXPRTEngine que pode gerar com eficiência simulações de PRT (transferência de radiante) precomputadas de uma cena 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Função D3DXCreatePRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506486"
---
# <a name="d3dxcreateprtengine-function"></a>Função D3DXCreatePRTEngine

Cria um objeto [**ID3DXPRTEngine**](id3dxprtengine.md) que pode gerar com eficiência simulações de PRT (transferência de radiante) precomputadas de uma cena 3D.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) de entrada que modela a cena 3D. Essa malha deve ter uma tabela de atributos na qual os vértices estão em um atributo exclusivo.

</dd> <dt>

*pAdjacency* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro opcional para uma matriz de três DWORDs por face a ser preenchida com índices de face adjacentes. O número de bytes nessa matriz deve ser pelo menos (3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)). Pode ser **NULL**.

</dd> <dt>

*ExtractUVs* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **for true**, as texturas serão usadas para armazenar os vetores ALBEDOS ou PRT.

</dd> <dt>

*pBlockerMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) opcional que bloqueia a cena 3D. Pode ser **NULL**.

</dd> <dt>

*ppEngine* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**

Ponteiro para um objeto [**ID3DXPRTEngine**](id3dxprtengine.md) de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) para combinar várias malhas em uma única interface de malha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
