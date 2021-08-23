---
description: Defina dados de vértice em um dos buffers de vértice da malha.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'Método ID3DX10Mesh:: SetVertexData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59dc5292d5d5dfc269f97f2a8d19ce9a19ea95ceefda47eaf89ac77f81838f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990326"
---
# <a name="id3dx10meshsetvertexdata-method"></a>Método ID3DX10Mesh:: SetVertexData

Defina dados de vértice em um dos buffers de vértice da malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iBuffer* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O buffer de vértice a ser preenchido com pData.

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Tipo: **const void \***

Os dados de vértice a serem definidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
