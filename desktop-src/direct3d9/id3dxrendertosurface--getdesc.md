---
description: Recupera os parâmetros da superfície de renderização.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'Método ID3DXRenderToSurface:: GetDesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7dd6787ad8a81491e92af2a5ec1a16253af4cd0a0f8cb075dde01461b0010d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790476"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>Método ID3DXRenderToSurface:: GetDesc

Recupera os parâmetros da superfície de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pParameters* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXRTS \_ desc**](d3dxrts-desc.md)\***

Ponteiro para uma [**estrutura \_ desc de D3DXRTS**](d3dxrts-desc.md) , descrevendo os parâmetros da superfície de renderização.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 




