---
description: Reamostrar um buffer ID3DXPRTBuffer de entrada e salvá-lo em um buffer de saída. Esse método pode ser usado para converter um buffer de vértice em um buffer de textura e vice-versa. Ele também pode ser usado para converter buffers de canal único em buffers de 3 canais e vice-versa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: 'Método ID3DXPRTEngine:: ResampleBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664086"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>Método ID3DXPRTEngine:: ResampleBuffer

Reamostrar um buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada e salvá-lo em um buffer de saída. Esse método pode ser usado para converter um buffer de vértice em um buffer de textura e vice-versa. Ele também pode ser usado para converter buffers de canal único em buffers de 3 canais e vice-versa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBufferIn* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para o buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada.

</dd> <dt>

*pBufferOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para o buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 




