---
description: Adiciona outro buffer ao ID3DXPRTBuffer e armazena os resultados em ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'Método ID3DXPRTBuffer:: addbuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764427"
---
# <a name="id3dxprtbufferaddbuffer-method"></a>Método ID3DXPRTBuffer:: addbuffer

Adiciona outro buffer ao [**ID3DXPRTBuffer**](id3dxprtbuffer.md) e armazena os resultados em **ID3DXPRTBuffer**.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBuffer* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ponteiro para um buffer que contém membros a serem adicionados aos respectivos membros do buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado.

## <a name="remarks"></a>Comentários

pBuffer e [**ID3DXPRTBuffer**](id3dxprtbuffer.md) devem ter o mesmo número de amostras, coeficientes e canais de cores; caso contrário, o método falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




