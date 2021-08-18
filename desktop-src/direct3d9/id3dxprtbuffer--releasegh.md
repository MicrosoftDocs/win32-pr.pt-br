---
description: Desassocia um objeto ID3DXTextureGutterHelper anexado ao objeto ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'Método ID3DXPRTBuffer:: ReleaseGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5691fc2601624733bb8d41b63140b694bd78027e0f6d548b02984bbc12406a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120530"
---
# <a name="id3dxprtbufferreleasegh-method"></a>Método ID3DXPRTBuffer:: ReleaseGH

Desassocia um objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) anexado ao objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Esse método libera o ponteiro para a interface [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .

Você deve garantir que o número de chamadas [**ID3DXPRTBuffer:: AttachGH**](id3dxprtbuffer--attachgh.md) corresponda ao número de chamadas **ID3DXPRTBuffer:: ReleaseGH** . Depois de chamar **ID3DXPRTBuffer:: ReleaseGH**, o ponteiro PGH retornado por **ID3DXPRTBuffer:: AttachGH** não deve mais ser usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




