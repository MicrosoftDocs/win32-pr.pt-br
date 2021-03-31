---
description: Encerra uma cena.
ms.assetid: f721593e-6cba-4569-8276-6a4ffc0fc37a
title: 'Método ID3DXRenderToSurface:: endcena (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.EndScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5aa0c1fbccb756ac612b813ad151813a782b122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663987"
---
# <a name="id3dxrendertosurfaceendscene-method"></a>Método ID3DXRenderToSurface:: EndScene

Encerra uma cena.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndScene(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MipFilter* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opções de filtro, enumeradas [no \_ filtro D3DX](d3dx-filter.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> <dt>

[**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md)
</dt> </dl>

 

 
