---
description: Obtém o máximo de influências de face em uma malha de triângulo com o buffer de índice especificado.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: Método ID3DXSkinInfo::GetMaxFaceInfluences (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 84e949c0b6140b4be0f55c47c0f24b3e3b2843009c5c0cd039c76caefa0667a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800665"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a>Método ID3DXSkinInfo::GetMaxFaceInfluences

Obtém o máximo de influências de face em uma malha de triângulo com o buffer de índice especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIB* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**

Ponteiro para o buffer de índice que contém os dados de índice de malha.

</dd> <dt>

*NumFaces* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de faces na malha.

</dd> <dt>

*maxFaceInfluences* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

O ponteiro para o rosto máximo influencia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
