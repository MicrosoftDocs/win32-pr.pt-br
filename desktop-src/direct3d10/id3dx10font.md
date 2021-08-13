---
description: A interface ID3DX10Font encapsula as texturas e os recursos necessários para renderizar uma fonte específica em um dispositivo específico.
ms.assetid: 81f4ffe3-f50d-47ce-ae85-15a2a19cacbd
title: Interface ID3DX10Font (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b40230aa983154f9bfc85b3ffb0f08f713b00213259d18bb9b160374b670795
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540342"
---
# <a name="id3dx10font-interface"></a>Interface ID3DX10Font

A interface ID3DX10Font encapsula as texturas e os recursos necessários para renderizar uma fonte específica em um dispositivo específico.

## <a name="members"></a>Membros

A interface **ID3DX10Font** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Font** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10Font** tem esses métodos.



| Método                                                     | Descrição                                                                                                                                           |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Drawtext**](id3dx10font-drawtext.md)                   | Desenhar texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.<br/>                                                                        |
| [**Getdc**](id3dx10font-getdc.md)                         | Retornar um alça para um DC (contexto de dispositivo de exibição) que tenha a fonte definida nele.<br/>                                                            |
| [**GetDesc**](id3dx10font-getdesc.md)                     | Obter uma descrição do objeto de fonte atual.<br/>                                                                                              |
| [**GetDevice**](id3dx10font-getdevice.md)                 | Recupere o dispositivo Direct3D associado ao objeto de fonte.<br/>                                                                              |
| [**GetGlyphData**](id3dx10font-getglyphdata.md)           | Retornar informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.<br/>                                                     |
| [**Gettextmetrics**](id3dx10font-gettextmetrics.md)       | Recuperar características de fonte.<br/>                                                                                                             |
| [**PreloadCharacters**](id3dx10font-preloadcharacters.md) | Carregue uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.<br/>                                        |
| [**Pré-loadGlyphs**](id3dx10font-preloadglyphs.md)         | Carregue uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.<br/>                                            |
| [**PreloadText**](id3dx10font-preloadtext.md)             | Carregue o texto formatado na memória de vídeo para melhorar a eficiência da renderização para o dispositivo. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.<br/> |



 

## <a name="remarks"></a>Comentários

A interface ID3DX10Font é obtida chamando [**D3DX10CreateFont**](d3dx10createfont.md) ou [**D3DX10CreateFontIndirect.**](d3dx10createfontindirect.md)

O tipo LPD3DX10FONT é definido como um ponteiro para a interface ID3DX10Font.


```
typedef interface ID3DX10Font ID3DX10Font;
typedef interface ID3DX10Font *LPD3DX10FONT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
