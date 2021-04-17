---
description: 'Acesse o buffer de índice da malha depois que ele tiver sido confirmado no dispositivo com ID3DX10Mesh:: CommitToDevice. Isso é diferente de ID3DX10Mesh:: GetIndexBuffer, que retorna o buffer de índice antes de ser confirmado no dispositivo.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'Método ID3DX10Mesh:: GetDeviceIndexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813309"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>Método ID3DX10Mesh:: GetDeviceIndexBuffer

Acesse o buffer de índice da malha depois que ele tiver sido confirmado no dispositivo com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Isso é diferente de [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), que retorna o buffer de índice antes de ser confirmado no dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppIndexBuffer* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

O buffer de índice depois de ter sido confirmado no dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Se o buffer de índice da malha ainda não tiver sido confirmado no dispositivo, essa API confirmará automaticamente o buffer de índice antes de retornar um ponteiro para o buffer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




