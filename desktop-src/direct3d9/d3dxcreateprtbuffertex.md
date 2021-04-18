---
description: Cria um buffer de PRT (transferência radiante em computação) que pode ser compactado ou preenchido por um simulador. Essa função deve ser usada para criar buffers por pixel.
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: Função D3DXCreatePRTBufferTex (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3e88073f85d281e164c002ba5180493f6217e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764275"
---
# <a name="d3dxcreateprtbuffertex-function"></a>Função D3DXCreatePRTBufferTex

Cria um buffer de PRT (transferência radiante em computação) que pode ser compactado ou preenchido por um simulador. Essa função deve ser usada para criar buffers por pixel.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Largura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Largura da textura, em pixels.

</dd> <dt>

*Altura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altura da textura, em pixels.

</dd> <dt>

*NumCoeffs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de coeficientes por local de exemplo. Ao usar o PRT harmônica (SH) de esférico, o número de coeficientes deve ser pedido ², em que Order é a ordem da avaliação SH. A ordem deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. O grau da avaliação é a ordem 1.

</dd> <dt>

*NumChannels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de canais de cores a serem definidos na malha. Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.

</dd> <dt>

*ppBuffer* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Quando o buffer é criado, todos os valores são inicializados como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
