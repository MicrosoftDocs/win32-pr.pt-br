---
description: Carrega uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: 'ID3DXFont: método reloadGlyphs de:P (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012172"
---
# <a name="id3dxfontpreloadglyphs-method"></a>ID3DXFont: método reloadGlyphs de:P

Carrega uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Primeiro* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID do primeiro glifo a ser carregado na memória de vídeo.

</dd> <dt>

*Último* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID do último glifo a ser carregado na memória de vídeo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Esse método gera texturas que contêm os glifos de entrada. Os glifos são desenhados como uma série de triângulos.

Os glifos não serão renderizados para o dispositivo; O [**DrawText**](id3dxfont--drawtext.md) ainda deve ser chamado para renderizar os glifos. No entanto, ao pré-carregar glifos na memória de vídeo, o **DrawText** usará substancialmente menos recursos de CPU.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
