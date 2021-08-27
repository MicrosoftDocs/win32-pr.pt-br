---
description: Multiplica cada valor no buffer por um valor constante.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'Método ID3DXPRTBuffer:: ScaleBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5cba39f6816e301f2d36e21e6f81c7bb1f6bb4792fe4ea8017de5d452faf357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801484"
---
# <a name="id3dxprtbufferscalebuffer-method"></a>Método ID3DXPRTBuffer:: ScaleBuffer

Multiplica cada valor no buffer por um valor constante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Escala* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor constante usado para dimensionar o buffer. Cada valor no buffer é substituído pelo produto desse valor e pelo valor do buffer original.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
