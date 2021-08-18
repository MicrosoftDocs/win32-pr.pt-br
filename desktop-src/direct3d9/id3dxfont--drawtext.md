---
description: Desenha texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: 'ID3DXFont: método rawText de:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d2a0b2dc61e2dd2a41f5a2fe864973fca91a5e471c75d6afc353c147f7a00fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987416"
---
# <a name="id3dxfontdrawtext-method"></a>ID3DXFont: método rawText de:D

Desenha texto formatado. Esse método dá suporte a cadeias de caracteres ANSI e Unicode.

## <a name="syntax"></a>Sintaxe


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSprite* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)**

Ponteiro para um objeto [**ID3DXSprite**](id3dxsprite.md) que contém a cadeia de caracteres. Pode ser **NULL**; nesse caso, o Direct3D renderizará a cadeia de caracteres com seu próprio objeto Sprite. Para melhorar a eficiência, um objeto Sprite deve ser especificado se o **DrawText** for ser chamado mais de uma vez em uma linha.

</dd> <dt>

*pString* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Ponteiro para uma cadeia de caracteres a ser desenhada. Se o parâmetro Count for-1, a cadeia de caracteres deverá ser terminada em nulo.

</dd> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Especifica o número de caracteres na cadeia de caracteres. Se Count for-1, o parâmetro pString será considerado como um ponteiro para uma cadeia de caracteres terminada em nulo e o **DrawText** calculará automaticamente a contagem de caracteres.

</dd> <dt>

*pRect* \[ no\]
</dt> <dd>

Tipo: **[ **lpRect**](../winprog/windows-data-types.md)**

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado. O valor da coordenada do lado direito do retângulo deve ser maior do que o do lado esquerdo. Da mesma forma, o valor da coordenada da parte inferior deve ser maior que o da parte superior.

</dd> <dt>

*Formato* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o método de formatação do texto. Pode ser qualquer combinação dos seguintes valores:



| Valor                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <dt>**\_parte inferior de DT**</dt> </dl>             | Justifica o texto na parte inferior do retângulo. Esse valor deve ser combinado com \_ uma única de DT.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <dt>**\_CALCRECT DT**</dt> </dl>       | Determina a largura e a altura do retângulo. Se houver várias linhas de texto, o **DrawText** usará a largura do retângulo apontado pelo parâmetro pRect e estenderá a base do retângulo para associar a última linha de texto. Se houver apenas uma linha de texto, **DrawText** modificará o lado direito do retângulo para que ele limite o último caractere na linha. Em ambos os casos, **DrawText** retorna a altura do texto formatado, mas não desenha o texto.<br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <dt>**Centro de DT \_**</dt> </dl>             | Centraliza o texto horizontalmente no retângulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <dt>**\_EXPANDTABS DT**</dt> </dl> | Amplia os caracteres da guia. O número padrão de caracteres por guia é oito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <dt>**DT \_ restante**</dt> </dl>                   | Alinha o texto à esquerda.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <dt>**noclip de DT \_**</dt> </dl>             | Desenha sem recorte. O **DrawText** é um pouco mais rápido quando o DT \_ noclip é usado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <dt>**DT \_ à direita**</dt> </dl>                | Alinha o texto à direita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <dt>**\_RTLREADING DT**</dt> </dl> | Exibe o texto na ordem de leitura da direita para a esquerda para texto bidirecional quando uma fonte hebraico ou árabe é selecionada. A ordem de leitura padrão para todo o texto é da esquerda para a direita.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <dt>**única de DT \_**</dt> </dl> | Exibe o texto somente em uma única linha. Retornos de carro e feeds de linha não quebram a linha.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <dt>**início da DT \_**</dt> </dl>                      | Justifica o texto na parte superior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <dt>**\_VCENTER DT**</dt> </dl>          | Centraliza o texto verticalmente (somente linha única).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <dt>**\_justificação DT**</dt> </dl>    | Quebra palavras. As linhas são quebradas automaticamente entre as palavras se uma palavra ultrapassar a borda do retângulo especificado pelo parâmetro pRect. Uma sequência de retorno de carro/alimentação de linha também quebra a linha.<br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

*Cor* \[ do no\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Cor do texto. Para obter mais informações, consulte [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **int**](../winprog/windows-data-types.md)**

Se a função for realizada com sucesso, o valor de retorno será a altura do texto em unidades lógicas. Se \_ \_ a parte inferior de DT VCENTER ou DT for especificada, o valor de retorno será o deslocamento de pRect (superior à parte inferior) do texto desenhado. Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Os parâmetros desse método são muito semelhantes aos da função [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) do GDI.

Esse método dá suporte a cadeias de caracteres ANSI e Unicode.

Este método deve ser chamado dentro de um [**BeginScene**](/windows/desktop/api) ... Bloco [**endcena**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) . A única exceção é quando um aplicativo chama **DrawText** com \_ CALCRECT DT para calcular o tamanho de um determinado bloco de texto.

A menos que o \_ formato noclip de DT seja usado, esse método corta o texto para que ele não apareça fora do retângulo especificado. É presumida que toda a formatação tenha várias linhas, a menos que o formato de linha \_ simples DT seja especificado.

Se a fonte selecionada for muito grande para o retângulo, esse método não tentará substituir uma fonte menor.

Esse método dá suporte apenas a fontes cuja escape e orientação são zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
