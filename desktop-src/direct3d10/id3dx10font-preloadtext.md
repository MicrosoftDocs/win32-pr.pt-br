---
description: Carregue o texto formatado na memória de vídeo para melhorar a eficiência da renderização para o dispositivo. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: 'ID3DX10Font: método reloadText de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173021"
---
# <a name="id3dx10fontpreloadtext-method"></a>ID3DX10Font: método reloadText de:P

Carregue o texto formatado na memória de vídeo para melhorar a eficiência da renderização para o dispositivo. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pString* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

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

O texto não será renderizado para o dispositivo; ID3DX10Font::D rawText ainda deve ser chamado para renderizar o texto. No entanto, ao carregar texto em memória de vídeo, ID3DX10Font:D: o rawText usará substancialmente menos recursos de CPU.

Esse método converte internamente os caracteres em glifos usando a função GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
