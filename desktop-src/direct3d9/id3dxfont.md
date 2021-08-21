---
description: A interface ID3DXFont encapsula as texturas e os recursos necessários para processar uma fonte específica em um dispositivo específico.
ms.assetid: ac40b600-3b9f-4e6e-8563-18597b3dd602
title: Interface ID3DXFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f05322ef2d7898f0025154989e9ac09ab8355025d8ad1ed94034fb25da66592f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493646"
---
# <a name="id3dxfont-interface"></a>Interface ID3DXFont

A interface ID3DXFont encapsula as texturas e os recursos necessários para processar uma fonte específica em um dispositivo específico.

## <a name="members"></a>Membros

A interface **ID3DXFont** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFont** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXFont** tem esses métodos.



| Método                                                    | Descrição                                                                                                                                                                                                                                   |
|:----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText**](id3dxfont--drawtext.md)                   | Desenha texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.<br/>                                                                                                                                                               |
| [**GetDC**](id3dxfont--getdc.md)                         | Retorna um identificador para um contexto de dispositivo de exibição (DC) que tem o conjunto de fontes.<br/>                                                                                                                                                           |
| [**GetDesc**](id3dxfont--getdesc.md)                     | Obtém uma descrição do objeto de fonte atual. GetDescW e getdescum são idênticos a esse método, exceto que um ponteiro é retornado para uma estrutura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) ou **D3DXFONT \_ desca** , respectivamente.<br/> |
| [**GetDevice**](id3dxfont--getdevice.md)                 | Recupera o dispositivo Direct3D associado ao objeto Font.<br/>                                                                                                                                                                     |
| [**GetGlyphData**](id3dxfont--getglyphdata.md)           | Retorna informações sobre o posicionamento e a orientação de um glifo em uma célula de caractere.<br/>                                                                                                                                            |
| [**GetTextMetrics**](id3dxfont--gettextmetrics.md)       | Recupera características de fonte que são identificadas em uma estrutura [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Esse método dá suporte às configurações de compilador ANSI e Unicode.<br/>                                                                       |
| [**OnLostDevice**](id3dxfont--onlostdevice.md)           | Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.<br/>                                              |
| [**OnResetDevice**](id3dxfont--onresetdevice.md)         | Use este método para readquirir recursos e salvar o estado inicial.<br/>                                                                                                                                                                    |
| [**PreloadCharacters**](id3dxfont--preloadcharacters.md) | Carrega uma série de caracteres na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.<br/>                                                                                                                               |
| [**PreloadGlyphs**](id3dxfont--preloadglyphs.md)         | Carrega uma série de glifos na memória de vídeo para melhorar a eficiência da renderização para o dispositivo.<br/>                                                                                                                                   |
| [**PreloadText**](id3dxfont--preloadtext.md)             | Carrega texto formatado em memória de vídeo para melhorar a eficiência da renderização para o dispositivo. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.<br/>                                                                                        |



 

## <a name="remarks"></a>Comentários

A interface **ID3DXFont** é obtida chamando [**D3DXCreateFont**](d3dxcreatefont.md) ou [**D3DXCreateFontIndirect**](d3dxcreatefontindirect.md).

O tipo LPD3DXFONT é definido como um ponteiro para a interface **ID3DXFont** .


```
typedef interface ID3DXFont ID3DXFont;
typedef interface ID3DXFont *LPD3DXFONT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
