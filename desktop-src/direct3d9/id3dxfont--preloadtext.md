---
description: Carrega texto formatado em memória de vídeo para melhorar a eficiência da renderização para o dispositivo. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: 'ID3DXFont: método reloadText de:P (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091997"
---
# <a name="id3dxfontpreloadtext-method"></a>ID3DXFont: método reloadText de:P

Carrega texto formatado em memória de vídeo para melhorar a eficiência da renderização para o dispositivo. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pString* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***

Ponteiro para uma cadeia de caracteres a ser carregada na memória de vídeo. Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR; caso contrário, o tipo de dados será resolvido para LPCSTR. Consulte Observações.

</dd> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Número de caracteres na cadeia de texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como PreloadTextW. Caso contrário, a chamada de função é resolvida como PreloadTextA porque as cadeias de caracteres ANSI estão sendo usadas.

Esse método gera texturas que contêm glifos que representam o texto de entrada. Os glifos são desenhados como uma série de triângulos.

O texto não será renderizado para o dispositivo; O [**DrawText**](id3dxfont--drawtext.md) ainda deve ser chamado para renderizar o texto. No entanto, ao carregar texto em memória de vídeo, o **DrawText** usará substancialmente menos recursos de CPU.

Esse método converte internamente os caracteres em glifos usando a função GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
