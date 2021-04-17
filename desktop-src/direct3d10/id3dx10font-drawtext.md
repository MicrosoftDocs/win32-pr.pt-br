---
description: Desenhar texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: 'ID3DX10Font: método rawText de:D (D3DX10. h)'
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
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813457"
---
# <a name="id3dx10fontdrawtext-method"></a>ID3DX10Font: método rawText de:D

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

*pSprite* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**

Ponteiro para um objeto ID3DX10Sprite que contém a cadeia de caracteres que você deseja desenhar. Pode ser **NULL**; nesse caso, o Direct3D renderizará a cadeia de caracteres com seu próprio objeto Sprite. Para melhorar a eficiência, um objeto Sprite deve ser especificado se ID3DX10Font::D rawText for ser chamado mais de uma vez em uma linha.

</dd> <dt>

*pString* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres a ser desenhada. Se o UNICODE estiver definido, esse tipo de parâmetro será resolvido como um LPCWSTR, caso contrário, o tipo será resolvido para um LPCSTR. Se o parâmetro Count for-1, a cadeia de caracteres deverá ser terminada como **NULL** .

</dd> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

O número de caracteres na cadeia de caracteres. Se Count for-1, o parâmetro pString será considerado um ponteiro para um Sprite contendo uma cadeia de caracteres terminada em nulo e ID3DX10Font::D rawText calculará automaticamente a contagem de caracteres.

</dd> <dt>

*pRect* \[ no\]
</dt> <dd>

Tipo: **lpRect**

Ponteiro para uma estrutura [Rect](/previous-versions//ms536136(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado. Assim como ocorre com qualquer objeto RECT, o valor da coordenada do lado direito do retângulo deve ser maior do que o do lado esquerdo. Da mesma forma, o valor da coordenada da parte inferior deve ser maior que o da parte superior.

</dd> <dt>

*Formato* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Especifique o método de formatação do texto. Pode ser qualquer combinação dos seguintes valores:



| Item                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span>\_parte inferior de DT<br/>             | Justifique o texto na parte inferior do retângulo. Esse valor deve ser combinado com \_ uma única de DT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>\_CALCRECT DT<br/>       | Diga ao DrawText para calcular automaticamente a largura e a altura do retângulo com base no comprimento da cadeia de caracteres que você o informa para desenhar. Se houver várias linhas de texto, ID3DX10Font::D rawText usará a largura do retângulo apontado pelo parâmetro pRect e estenderá a base do retângulo para associar a última linha de texto. Se houver apenas uma linha de texto, ID3DX10Font::D rawText modificar o lado direito do retângulo para que ele limite o último caractere na linha. Em ambos os casos, ID3DX10Font::D rawText retorna a altura do texto formatado, mas não desenha o texto.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span>Centro de DT \_<br/>             | Centralizar o texto horizontalmente no retângulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>\_EXPANDTABS DT<br/> | Expanda os caracteres de tabulação. O número padrão de caracteres por guia é oito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span>DT \_ restante<br/>                   | Alinhar texto à esquerda.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span>noclip de DT \_<br/>             | Desenhe sem recorte. ID3DX10Font::D rawText é um pouco mais rápido quando o DT \_ noclip é usado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RIGHT"></span><span id="dt_right"></span>DT \_ à direita<br/>                | Alinhar texto à direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>\_RTLREADING DT<br/> | Exibir texto na ordem de leitura da direita para a esquerda para texto bidirecional quando uma fonte hebraico ou árabe for selecionada. A ordem de leitura padrão para todo o texto é da esquerda para a direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>única de DT \_<br/> | Exibir texto somente em uma única linha. Retornos de carro e feeds de linha não quebram a linha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span>início da DT \_<br/>                      | Justifica o texto de cima para baixo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span>\_VCENTER DT<br/>          | Centralizar texto verticalmente (somente linha única).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>\_justificação DT<br/>    | Quebrar palavras. As linhas são quebradas automaticamente entre as palavras se uma palavra ultrapassar a borda do retângulo especificado pelo parâmetro pRect. Uma sequência de retorno de carro/alimentação de linha também quebra a linha.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Cor* \[ do no\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

Cor do texto. Consulte [**D3DXCOLOR**](d3d10-d3dxcolor.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Se a função for realizada com sucesso, o valor de retorno será a altura do texto em unidades lógicas. Se \_ \_ a parte inferior de DT VCENTER ou DT for especificada, o valor de retorno será o deslocamento de pRect (superior à parte inferior) do texto desenhado. Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Os parâmetros desse método são muito semelhantes aos da função DrawText do [GDI](/previous-versions//ms533909(v=vs.85)) .

Esse método dá suporte a cadeias de caracteres ANSI e Unicode.

A menos que o \_ formato noclip de DT seja usado, esse método corta o texto para que ele não apareça fora do retângulo especificado. É presumida que toda a formatação tenha várias linhas, a menos que o formato de linha \_ simples DT seja especificado.

Se a fonte selecionada for muito grande para o retângulo, esse método não tentará substituir uma fonte menor.

Esse método dá suporte apenas a fontes cuja escape e orientação são zero.

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

 

 
