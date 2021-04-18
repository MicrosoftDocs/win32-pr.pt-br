---
description: Carregue uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: 'ID3DX10Font: método reloadCharacters de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780906"
---
# <a name="id3dx10fontpreloadcharacters-method"></a>ID3DX10Font: método reloadCharacters de:P

Carregue uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Primeiro* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID do primeiro caractere a ser carregado na memória de vídeo.

</dd> <dt>

*Último* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

ID do último caractere a ser carregado na memória de vídeo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Esse método gera texturas contendo glifos que representam os caracteres de entrada. Os glifos são desenhados como uma série de triângulos.

Os caracteres não serão renderizados para o dispositivo; ID3DX10Font::D rawText ainda deve ser chamado para renderizar os caracteres. No entanto, ao pré-carregar caracteres na memória de vídeo, ID3DX10Font:D: o rawText usará substancialmente menos recursos de CPU.

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

 

 
