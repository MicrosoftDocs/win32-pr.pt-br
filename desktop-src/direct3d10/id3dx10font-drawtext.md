---
description: Desenhar texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: Método ID3DX10Font::D rawText (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1eabe3a88fb3d38021eee8f186baed1d8403d18026d4d1704d520ad3c8b8f72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303166"
---
# <a name="id3dx10fontdrawtext-method"></a>Método ID3DX10Font::D rawText

Desenhar texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.

## <a name="syntax"></a>Sintaxe


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSprite* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Ponteiro para um objeto ID3DX10Sprite que contém a cadeia de caracteres que você deseja desenhar. Pode ser **NULL,** caso em que o Direct3D renderizará a cadeia de caracteres com seu próprio objeto sprite. Para melhorar a eficiência, um objeto sprite deverá ser especificado se ID3DX10Font::D rawText for chamado mais de uma vez em uma linha.

</dd> <dt>

*pString* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres a ser desenhada. Se UNICODE for definido, esse tipo de parâmetro será resolvido para um LPCWSTR; caso contrário, o tipo será resolvido para um LPCSTR. Se o parâmetro Count for -1, a cadeia de caracteres deverá ser **terminada em NULL.**

</dd> <dt>

*Contagem* \[ Em\]
</dt> <dd>

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

O número de caracteres na cadeia de caracteres. Se Count for -1, o parâmetro pString será presumido como um ponteiro para um sprite que contém uma cadeia de caracteres terminada em NULL e ID3DX10Font::D rawText calculará a contagem de caracteres automaticamente.

</dd> <dt>

*pRect* \[ Em\]
</dt> <dd>

Tipo: **LPRECT**

Ponteiro para uma [estrutura RECT](/previous-versions//ms536136(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado. Assim como com qualquer objeto RECT, o valor da coordenada do lado direito do retângulo deve ser maior que o do lado esquerdo. Da mesma forma, o valor da coordenada da parte inferior deve ser maior que o da parte superior.

</dd> <dt>

*Formato* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Especifique o método de formatação do texto. Pode ser qualquer combinação dos seguintes valores:



| Item                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ BOTTOM<br/>             | Justifique o texto na parte inferior do retângulo. Esse valor deve ser combinado com DT \_ SINGLELINE.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT<br/>       | Diga a DrawText para calcular automaticamente a largura e a altura do retângulo com base no comprimento da cadeia de caracteres que você diz para desenhar. Se houver várias linhas de texto, ID3DX10Font::D rawText usará a largura do retângulo apontado pelo parâmetro pRect e estenderá a base do retângulo para delimitar a última linha de texto. Se houver apenas uma linha de texto, ID3DX10Font::D rawText modificará o lado direito do retângulo para que ele limite o último caractere na linha. Em ambos os casos, ID3DX10Font::D rawText retorna a altura do texto formatado, mas não desenha o texto.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>DT \_ CENTER<br/>             | Centralizar texto horizontalmente no retângulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ EXPANDTABS<br/> | Expanda caracteres de tabulação. O número padrão de caracteres por guia é oito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ LEFT<br/>                   | Alinhe o texto à esquerda.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>NOCLIP de DT \_<br/>             | Desenhar sem recorte. ID3DX10Font::D rawText é um pouco mais rápido quando o DT \_ NOCLIP é usado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>DT \_ RIGHT<br/>                | Alinhe o texto à direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING<br/> | Exibir texto na ordem de leitura da direita para a esquerda para texto bidirecional quando uma fonte hebraico ou árabe é selecionada. A ordem de leitura padrão para todo o texto é da esquerda para a direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ SINGLELINE<br/> | Exibir texto somente em uma única linha. Retornos de carro e alimentação de linha não quebram a linha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>DT \_ TOP<br/>                      | Texto mais justificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT \_ VCENTER<br/>          | Centralizar o texto verticalmente (somente linha única).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WORDBREAK<br/>    | Palavras de quebra. As linhas serão divididas automaticamente entre palavras se uma palavra se estender além da borda do retângulo especificado pelo parâmetro pRect. Uma sequência de retorno de carro/alimentação de linha também interrompe a linha.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Cor* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Cor do texto. Consulte [**D3DXCOLOR**](d3d10-d3dxcolor.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **INT**](../winprog/windows-data-types.md)**

Se a função for bem-sucedida, o valor de retorno será a altura do texto em unidades lógicas. Se DT VCENTER ou DT BOTTOM for especificado, o valor de retorno será o deslocamento de \_ pRect (de cima para baixo) do \_ texto desenhado. Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Os parâmetros desse método são muito semelhantes aos da [função DrawText GDI.](/previous-versions//ms533909(v=vs.85))

Esse método dá suporte a cadeias de caracteres ANSI e Unicode.

A menos que o formato NOCLIP de DT seja usado, esse método clipes de texto para que ele \_ não apareça fora do retângulo especificado. Supõe-se que toda a formatação tenha várias linhas, a menos que o formato DT \_ SINGLELINE seja especificado.

Se a fonte selecionada for muito grande para o retângulo, esse método não tentará substituir uma fonte menor.

Esse método dá suporte apenas a fontes cujo escape e orientação são zero.

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

 

 
