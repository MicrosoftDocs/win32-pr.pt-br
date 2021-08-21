---
description: Acesse o buffer de adjacency da malha.
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: Método ID3DX10Mesh::GetAdjacencyBuffer (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a26c6c1ecf90b4cdbc7f362be04960b6a53467124a583017ea87cd8fbcec6951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046934"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a>Método ID3DX10Mesh::GetAdjacencyBuffer

Acesse o buffer de adjacency da malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

O buffer de adjacency. Consulte [**ID3DX10MeshBuffer.**](id3dx10meshbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




