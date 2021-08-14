---
description: Carregue uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: Método ID3DX10Font::P reloadGlyphs (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 358523135db83f2ec7f973fce403a44d2f0ece82ab60cf9527cb612ccde61e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540332"
---
# <a name="id3dx10fontpreloadglyphs-method"></a>Método ID3DX10Font::P reloadGlyphs

Carregue uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Primeiro* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

ID do primeiro glifo a ser carregado na memória de vídeo.

</dd> <dt>

*Último* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

ID do último glifo a ser carregado na memória de vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Esse método gera texturas que contêm os glifos de entrada. Os glifos são desenhados como uma série de triângulos.

Os glifos não serão renderizados para o dispositivo; ID3DX10Font::D rawText ainda deve ser chamado para renderizar os glifos. No entanto, ao pré-carregar glifos na memória de vídeo, ID3DX10Font::D rawText usará significativamente menos recursos de CPU.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
