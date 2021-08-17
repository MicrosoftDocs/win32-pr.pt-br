---
description: Transforma animações em um conjunto de animação em um formato compactado e retorna um ponteiro para o buffer que armazena os dados compactados.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: Método ID3DXKeyframedAnimationSet::Compress (D3dx9 bluetoothm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d444ffde525677715f64bd9641cc8fb3cf9513e2c8805a6be28b280aaa12e015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802383"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>Método ID3DXKeyframedAnimationSet::Compress

Transforma animações em um conjunto de animação em um formato compactado e retorna um ponteiro para o buffer que armazena os dados compactados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Um dos valores [**de SINALIZADORES \_ D3DXCOMPRESSION**](./d3dxcompression-flags.md) que definem o modo de compactação usado para armazenar dados de conjunto de animação compactado. D3DXCOMPRESS \_ DEFAULT é o único valor com suporte no momento.

</dd> <dt>

*Perda* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Taxa de perda de compactação desejada, no intervalo de 0 a 1.

</dd> <dt>

*pHierarchy* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Ponteiro para uma hierarquia [**de quadros de transformação D3DXFRAME.**](d3dxframe.md) Pode ser **NULL.**

</dd> <dt>

*ppCompressedData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para o conjunto de animação compactado [**ID3DXBuffer.**](id3dxbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
