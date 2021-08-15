---
description: Carrega uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: Método ID3DXFont::P reloadCharacters (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cad2a324a6a5d56ff88dd343cf091b8c4ff2b99cd829344ae91f364458ec51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295312"
---
# <a name="id3dxfontpreloadcharacters-method"></a>Método ID3DXFont::P reloadCharacters

Carrega uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Primeiro* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

ID do primeiro caractere a ser carregado na memória de vídeo.

</dd> <dt>

*Último* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

ID do último caractere a ser carregado na memória de vídeo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Esse método gera texturas que contêm glifos que representam os caracteres de entrada. Os glifos são desenhados como uma série de triângulos.

Os caracteres não serão renderizados para o dispositivo; [**DrawText**](id3dxfont--drawtext.md) ainda deve ser chamado para renderizar os caracteres. No entanto, ao pré-carregar caracteres na memória de vídeo, **DrawText** usará significativamente menos recursos de CPU.

Esse método converte internamente caracteres em glifos usando a função GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
