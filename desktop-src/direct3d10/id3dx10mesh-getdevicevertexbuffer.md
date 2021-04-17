---
description: 'Acesse o buffer de vértice da malha depois que ele tiver sido confirmado no dispositivo com ID3DX10Mesh:: CommitToDevice. Isso é diferente de ID3DX10Mesh:: GetVertexBuffer, que retorna o buffer de vértice antes de ser confirmado no dispositivo.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'Método ID3DX10Mesh:: GetDeviceVertexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787595"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a>Método ID3DX10Mesh:: GetDeviceVertexBuffer

Acesse o buffer de vértice da malha depois que ele tiver sido confirmado no dispositivo com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md). Isso é diferente de [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que retorna o buffer de vértice antes de ser confirmado no dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iBuffer* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um índice que identifica qual buffer de vértice deve ser acessado.

</dd> <dt>

*ppVertexBuffer* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

O buffer de vértice após ter sido confirmado no dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

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

 

 
