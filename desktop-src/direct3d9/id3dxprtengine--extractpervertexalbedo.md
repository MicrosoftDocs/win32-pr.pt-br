---
description: Copia valores de albedo por vértice de uma malha.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'Método ID3DXPRTEngine:: ExtractPerVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e094a7681c13e21cdaab71648b3733749fc179f845e23496a07f3c2b7b99234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747746"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>Método ID3DXPRTEngine:: ExtractPerVertexAlbedo

Copia valores de albedo por vértice de uma malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para o objeto de malha [**ID3DXMesh**](id3dxmesh.md) usado em [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) para criar o objeto [**ID3DXPRTEngine**](id3dxprtengine.md) .

</dd> <dt>

*Uso* \[ do no\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descrições de uso de vértice a serem copiadas da malha. Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*NumChanIn* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de canais de cores a serem copiados da malha. Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
