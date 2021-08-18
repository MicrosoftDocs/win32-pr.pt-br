---
description: Otimiza a malha de patches para mosaico eficiente.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'Método ID3DXPatchMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 245f3ddb2c85f5de6ae2acc040f929387d522c12d65eeb4d4307f162b8532af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120720"
---
# <a name="id3dxpatchmeshoptimize-method"></a>Método ID3DXPatchMesh:: Optimize

Otimiza a malha de patches para mosaico eficiente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Atualmente não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.

## <a name="remarks"></a>Comentários

Depois que um aplicativo gera informações de adjacência para uma malha, os dados de malha podem ser otimizados (reordenados) para melhorar o desempenho do desenho. Esse método determina quais patches são adjacentes (dentro da tolerância fornecida).

As informações de adjacência também são usadas para otimizar o mosaico. Gere informações de adjacência uma vez e incluí repetidamente chamando [**ID3DXPatchMesh:: incluí**](id3dxpatchmesh--tessellate.md). A otimização executada é independente do nível de mosaico real usado. No entanto, se os vértices de malha forem alterados, você deverá regenerar as informações de adjacência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
