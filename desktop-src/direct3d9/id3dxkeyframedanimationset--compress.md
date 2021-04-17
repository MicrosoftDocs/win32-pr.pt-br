---
description: Transforma animações em uma animação definida em um formato compactado e retorna um ponteiro para o buffer que armazena os dados compactados.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'Método ID3DXKeyframedAnimationSet:: compress (D3dx9anim. h)'
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
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763005"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>Método ID3DXKeyframedAnimationSet:: compress

Transforma animações em uma animação definida em um formato compactado e retorna um ponteiro para o buffer que armazena os dados compactados.

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

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Um dos valores [**de \_ sinalizadores D3DXCOMPRESSION**](./d3dxcompression-flags.md) que definem o modo de compactação usado para armazenar dados de conjunto de animação compactados. D3DXCOMPRESS \_ default é o único valor com suporte no momento.

</dd> <dt>

*Perda* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Taxa de perda de compactação desejada, no intervalo de 0 a 1.

</dd> <dt>

*pHierarchy* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Ponteiro para uma hierarquia de quadros de transformação [**D3DXFRAME**](d3dxframe.md) . Pode ser **NULL**.

</dd> <dt>

*ppCompressedData* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para o conjunto de animações compactadas [**ID3DXBuffer**](id3dxbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
