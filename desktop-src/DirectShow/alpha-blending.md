---
description: Mesclagem alfa
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Mesclagem alfa (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087835"
---
# <a name="alpha-blending-directshow"></a>Mesclagem alfa (DirectShow)

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Este artigo descreve a mistura alfa nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).

Alfa mede a transparência de um pixel ou imagem. No vídeo RGB não compactado de 32 bits, quatro componentes definem cada pixel: um canal alfa (A) e três componentes de cor (RGB). Um pixel com um valor alfa igual a zero é completamente transparente. Um pixel com um valor alfa de 255 é opaco. Entre esses valores, o pixel tem vários graus de transparência.

O DirectShow define dois tipos de mídia para vídeo RGB de 32 bits:

-   **MEDIASUBTYPE \_ ARGB32**: o vídeo é RGB de 32 bits com um canal alfa válido.
-   **MEDIASUBTYPE \_ RGB32**: os pixels são 32 bits, mas o canal alfa não é necessariamente válido.

Para executar a mesclagem alfa no DES, defina o tipo de mídia descompactado do grupo de vídeos como MEDIASUBTYPE \_ ARGB32. Em C++, chame o método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) . No formato XTL, definir o atributo [**bitdepth**](bitdepth-attribute.md) do elemento [**Group**](group-element.md) como 32 também realiza isso.

Em seguida, você precisa de dados de vídeo que contenham um canal alfa. Há várias opções:

-   Você pode usar um arquivo AVI que já tem vídeo RGB de 32 bits com dados alfa. Atualmente, o Alpha não tem suporte para arquivos de origem MPEG ou Microsoft Windows Media Format (WMF).
-   O DES dá suporte a arquivos de bitmap de 32 bits (. bmp) e de Targa (. tga) com dados alfa.
-   Você pode escrever um filtro de origem personalizado que cria dados RGB de 32 bits com Alfa. O tipo de mídia de saída deve ser **MEDIASUBTYPE \_ ARGB32**. Use o filtro como o subobjeto em um objeto de origem da linha do tempo.

Se a fonte de vídeo não tiver alfa, você poderá usar um efeito que cria dados alfa. O [efeito de setter alfa](alpha-setter-effect.md) define o canal alfa para a imagem inteira como um valor constante. Para variar o alfa ao longo do tempo, use a interface [**IPropertySetter**](ipropertysetter.md) com o efeito de setter alfa. A fonte original não precisa ser de 32 bits, desde que o tipo de mídia descompactado do grupo seja **MEDIASUBTYPE \_ ARGB32**.

Por fim, passe o vídeo para um efeito ou transição que executa a mistura alfa. A [transição do compositor](compositor-transition.md) executa a mesclagem alfa e a [transição de chave](key-transition.md) pode ser a chave por valor alfa.

O projeto de exemplo XTL a seguir executa a mesclagem alfa:


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os serviços de edição do DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



