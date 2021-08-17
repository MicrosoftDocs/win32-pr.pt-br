---
description: Recupera o índice do tipo de malha ao qual cada Texel pertence.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'Método ID3DXTextureGutterHelper:: GetFaceMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5fce4400b1f778581f830fff60ef4e1519ad73752da02f5194abe64f433d43c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729185"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a>Método ID3DXTextureGutterHelper:: GetFaceMap

Recupera o índice do tipo de malha ao qual cada Texel pertence.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFaceData* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para o índice da face de malha à qual cada Texel pertence.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentários

Os dados de face de malha retornados por esse método são válidos somente para texels válidos (não classe 0). [**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retornará valores diferentes de zero para texels válidos (não classe 0).

Para a [**classe 2 texels**](id3dxtexturegutterhelper.md), esse método recupera a face mais próxima.

O aplicativo deve alocar e gerenciar pFaceData.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
