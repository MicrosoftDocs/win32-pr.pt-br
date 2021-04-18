---
title: Elemento BANNER
description: O elemento BANNER define uma URL para um arquivo gráfico que será exibido no painel de exibição.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Elemento de faixa Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781277"
---
# <a name="banner-element"></a>Elemento BANNER

O elemento **banner** define uma URL para um arquivo gráfico que será exibido no painel de exibição.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Atributos

**Href** (obrigatório)

URL para um arquivo gráfico que é exibido no painel de exibição.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                   |
|-----------------|----------------------------|
| Elementos pai | **ASX**, **entrada**         |
| Elementos filho  | **abstract**, **moreinfo** |



 

## <a name="remarks"></a>Comentários

Esse elemento define uma URL para um arquivo gráfico que aparece no painel de exibição do Windows Media Player, sob o conteúdo do vídeo. Se a mídia for somente áudio, o gráfico de faixa será exibido por si só. O Windows Media Player reserva um espaço de 32 pixels de altura por 194 pixels de largura (a barra de faixa) para o gráfico. Se o gráfico definido na URL for menor que isso, ele será exibido em seu tamanho original. Se o elemento gráfico for maior do que o espaço reservado, o Windows Media Player cortará a imagem para se ajustar ao espaço.

Você pode usar um elemento **abstract** dentro do escopo do elemento **banner** para exibir o texto como uma dica de ferramenta quando o usuário pausa o ponteiro do mouse sobre o gráfico de faixa. Um elemento **moreinfo** dentro de um elemento **banner** define uma URL para a qual o usuário é levado quando o usuário clica no gráfico de faixa. (A URL pode ser qualquer caminho ou protocolo, como um link de email, uma URL de protocolo HTTP para um site ou até mesmo um comando do Microsoft JScript.) Quando o ponteiro é movido sobre o gráfico, o gráfico torna-se relevo e parece um botão.

Um elemento de **faixa** definido para um elemento **ASX** é exibido enquanto todos os clipes na playlist estão sendo reproduzidos. Um elemento de **faixa** definido em um elemento de **entrada** é exibido somente enquanto o clipe está sendo reproduzido e, durante esse tempo, substitui qualquer faixa definida dentro do elemento pai **ASX** . Você pode especificar como o player de mídia do Windows reserva espaço para a faixa definindo o atributo **BANNERBAR** do elemento **ASX** .

Não há suporte para imagens de banner com arquivos DRM ou quando o Windows Media Player está inserido em uma página da Web.

## <a name="examples"></a>Exemplos

Este é um exemplo de um elemento de **faixa** sem elementos filho:


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



Veja a seguir um exemplo de um elemento de **faixa** que contém elementos **abstract** e **moreinfo** .


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





