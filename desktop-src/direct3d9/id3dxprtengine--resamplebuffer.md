---
description: Resampla um buffer ID3DXPRTBuffer de entrada e salva-o em um buffer de saída. Esse método pode ser usado para converter um buffer de vértice em um buffer de textura e vice-versa. Ele também pode ser usado para converter buffers de canal único em buffers de três canais e vice-versa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: Método ID3DXPRTEngine::ResampleBuffer (D3DX9Mesh.h)
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
ms.openlocfilehash: aa945be7b01c928a5dc8f5e44a6a31e8cb6d879be102145d25e03e7bef73f3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729610"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>Método ID3DXPRTEngine::ResampleBuffer

Resampla um buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada e salva-o em um buffer de saída. Esse método pode ser usado para converter um buffer de vértice em um buffer de textura e vice-versa. Ele também pode ser usado para converter buffers de canal único em buffers de três canais e vice-versa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBufferIn* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para o buffer [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada.

</dd> <dt>

*pBufferOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para o buffer [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




