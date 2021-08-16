---
description: Associa um objeto ID3DXTextureGutterHelper ao objeto ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: Método ID3DXPRTBuffer::AttachGH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afb625c0f8db9d04737420ab386095bbe70b3e0f23e375f75c212da71e59b0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801944"
---
# <a name="id3dxprtbufferattachgh-method"></a>Método ID3DXPRTBuffer::AttachGH

Associa um [**objeto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) ao [**objeto ID3DXPRTBuffer.**](id3dxprtbuffer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGH* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Ponteiro para a [**interface ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) de um objeto que contém dados de medianiz de textura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

A contagem de referência do [**objeto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) será incrementada automaticamente em um. Todos os ponteiros **ID3DXTextureGutterHelper** existentes serão liberados.

Você deve garantir que o número de **chamadas ID3DXPRTBuffer::AttachGH** corresponde ao número de chamadas [**ID3DXPRTBuffer::ReleaseGH.**](id3dxprtbuffer--releasegh.md) Depois de chamar **ID3DXPRTBuffer::ReleaseGH**, o ponteiro pGH retornado por **ID3DXPRTBuffer::AttachGH** não deve mais ser usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




