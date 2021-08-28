---
description: Define o índice da face da malha à qual cada texel pertence.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: Método ID3DXTextureGutterHelper::SetFaceMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7de812f5445d0d8d704aeba939cf8cbc4441d4ed542bf716371a7fc12a1ba6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747376"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a>Método ID3DXTextureGutterHelper::SetFaceMap

Define o índice da face da malha à qual cada texel pertence.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFaceData* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Ponteiro para o índice da face da malha à qual cada texel pertence.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

A entrada de dados de face da malha para esse método é válida somente para os texels válidos (não classe 0). [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retornará valores diferentes de zero para os texels válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
