---
description: Altera o número de amostras contidas no buffer.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: 'Método ID3DXPRTBuffer:: resize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c54044ffc9e166131faa16c9b438b497c658ef25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807254"
---
# <a name="id3dxprtbufferresize-method"></a>Método ID3DXPRTBuffer:: Resize

Altera o número de amostras contidas no buffer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewSize* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de amostras a serem contidas no buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o seguinte valor será retornado, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
