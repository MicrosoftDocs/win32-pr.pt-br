---
description: Alterna o modo para desenhar linhas no estilo OpenGL.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'Método ID3DXLine:: SetGLLines (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 131c472ef4a2254880ef560edccb9c0cf1c8774b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837982"
---
# <a name="id3dxlinesetgllines-method"></a>Método ID3DXLine:: SetGLLines

Alterna o modo para desenhar linhas no estilo OpenGL.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bGLLines* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Alterna o desenho de linha em estilo OpenGL. **True** habilita linhas em estilo OpenGL e **false** habilita linhas em estilo Direct3D.

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

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
