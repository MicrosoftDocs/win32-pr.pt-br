---
title: Elemento BANNER
description: O elemento BANNER define uma URL para um arquivo gráfico que aparecerá no painel de exibição.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Elemento BANNER Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91b3de50c1360337c1344a1af1a0696361614dbc293390470e7c196e53528a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135959"
---
# <a name="banner-element"></a>Elemento BANNER

O **elemento BANNER** define uma URL para um arquivo gráfico que aparecerá no painel de exibição.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Atributos

**HREF** (obrigatório)

URL para um arquivo gráfico que é exibido no painel de exibição.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                   |
|-----------------|----------------------------|
| Elementos pai | **ASX**, **ENTRY**         |
| Elementos filho  | **ABSTRACT**, **MOREINFO** |



 

## <a name="remarks"></a>Comentários

Esse elemento define uma URL para um arquivo gráfico que aparece no painel Windows Media Player exibição, abaixo do conteúdo do vídeo. Se a mídia for somente áudio, o gráfico de faixa será exibido por si só. Windows Media Player reserva um espaço de 32 pixels de altura por 194 pixels de largura (a barra de faixas) para o gráfico. Se o gráfico definido na URL for menor que isso, ele será exibido em seu tamanho original. Se o gráfico for maior que o espaço reservado, Windows Media Player cortará a imagem para se ajustar ao espaço.

Você pode usar um **elemento ABSTRACT** dentro do escopo do elemento **BANNER** para exibir texto como uma Dica de Ferramenta quando o usuário pausa o ponteiro do mouse sobre o gráfico de faixa. Um **elemento MOREINFO** dentro de **um elemento BANNER** define uma URL para a qual o usuário é levado quando o usuário clica no gráfico de faixa. (A URL pode ser qualquer caminho ou protocolo, como um link de email, uma URL HTTP (Protocolo de Transferência de Hipertexto) para um site ou até mesmo um comando do Microsoft JScript.) Quando o ponteiro é movido sobre o gráfico, o gráfico se torna embossed e se parece com um botão.

Um **elemento BANNER** definido para um elemento **ASX** é exibido enquanto todos os clipes na playlist estão sendo exibidos. Um **elemento BANNER** definido em um elemento **ENTRY** é exibido somente enquanto esse clipe está sendo exibido e, durante esse tempo, substitui qualquer faixa definida dentro do elemento **ASX** pai. Você pode especificar como Windows Media Player reserva espaço para a faixa definindo o atributo **BANNERBAR** do **elemento ASX.**

Não há suporte para imagens de faixa com arquivos DRM ou quando Windows Media Player é inserido em uma página da Web.

## <a name="examples"></a>Exemplos

Veja a seguir um exemplo de um **elemento BANNER** sem elementos filho:


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



A seguir está um exemplo de um **elemento BANNER** que contém **elementos ABSTRACT** **e MOREINFO.**


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metadados de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





