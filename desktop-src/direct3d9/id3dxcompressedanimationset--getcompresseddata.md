---
description: Obtém o buffer de dados que armazena dados de animação de quadro-chave compactados.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: Método ID3DXCompressedAnimationSet::GetCompressedData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3290dcc9e9baeaa688117d8a98918e7df814a34812cb66791b2c8021a50f788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987576"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a>Método ID3DXCompressedAnimationSet::GetCompressedData

Obtém o buffer de dados que armazena dados de animação de quadro-chave compactados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppCompressedData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para o buffer de dados [**ID3DXBuffer**](id3dxbuffer.md) que recebe dados de animação de quadro-chave compactados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




