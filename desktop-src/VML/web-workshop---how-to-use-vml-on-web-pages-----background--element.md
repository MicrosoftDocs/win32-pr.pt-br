---
title: Usando o elemento background
description: Usando o elemento background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Workshop da Web, elemento background
- projetando páginas da Web, elemento de plano de fundo
- linguagem VML (VML), elemento background
- VML (linguagem VML), elemento background
- gráficos vetoriais, elemento background
- elemento background
- Elementos VML, plano de fundo
- Formas VML, elemento background
- linguagem VML (VML), personalização de plano de fundo
- VML (linguagem VML), personalização de segundo plano
- gráficos vetoriais, personalização de plano de fundo
- Formas VML, personalização de plano de fundo
- personalização de segundo plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb4a694aa5458a0eae01fcbf577f72da8b8f54b7efda506423565aee362ce2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512776"
---
# <a name="using-the-background-element"></a>Usando o elemento background

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Neste tópico, ilustramos como você pode personalizar o plano de fundo de uma página da Web usando o `<background>` elemento fornecido no VML.

Como você aprendeu no [ `<fill>` ](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) tópico Usar, você pode colocar o subconjunto dentro do , ou qualquer elemento de forma predefinido para descrever como `<fill>` preencher a `<shape>` `<shapetype>` forma.

Da mesma forma, você pode colocar o subconjunto dentro do elemento para descrever `<fill>` como preencher a plano de fundo de uma página da `<background>` Web. Em seguida, você pode usar os atributos de propriedade do subconjunto para personalizar o efeito de preenchimento, como preenchimento de gradiente, preenchimento de `<fill>` padrão ou preenchimento de [imagem.](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) [](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) [](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)

Por exemplo, para desenhar um plano de fundo preenchido com gradiente, você pode digitar as seguintes linhas `<BODY>` na região da página da Web:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 