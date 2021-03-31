---
title: Usando o elemento background
description: Usando o elemento background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Web Workshop, elemento de plano de fundo
- Criando páginas da Web, elemento de plano de fundo
- Linguagem VML (VML), elemento de plano de fundo
- VML (linguagem VML), elemento de segundo plano
- elementos gráficos vetoriais, elemento background
- elemento background
- Elementos de VML, plano de fundo
- Formas de VML, elemento de plano de fundo
- Linguagem VML (VML), personalizando planos de fundo
- VML (linguagem VML), personalizando planos de fundo
- gráficos vetoriais, personalizando planos de fundo
- Formas de VML, personalizando planos de fundo
- Personalizando planos de fundo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823817"
---
# <a name="using-the-background-element"></a>Usando o elemento background

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Neste tópico, Ilustraremos como você pode personalizar o plano de fundo de uma página da Web usando o `<background>` elemento fornecido em VML.

Como você aprendeu no tópico [ `<fill>` use](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , você pode posicionar o `<fill>` subelemento dentro do `<shape>` , `<shapetype>` ou qualquer elemento Shape predefinido para descrever como preencher a forma.

Da mesma forma, você pode posicionar o `<fill>` subelemento dentro do `<background>` elemento para descrever como preencher o plano de fundo de uma página da Web. Você pode usar os atributos de Propriedade do `<fill>` subelemento para personalizar o efeito de preenchimento, como [preenchimento gradual](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), preenchimento de [padrão](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)ou preenchimento de [imagem](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).

Por exemplo, para desenhar um plano de fundo preenchido com gradiente, você pode digitar as seguintes linhas na `<BODY>` região da sua página da Web:


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 