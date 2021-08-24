---
title: Usando o elemento Shadow
description: Usando o elemento Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Web Workshop, elemento Shadow
- Criando páginas da Web, elemento Shadow
- Linguagem VML (VML), elemento Shadow
- VML (linguagem VML), elemento Shadow
- gráficos vetoriais, elemento Shadow
- elemento Shadow
- Elementos de VML, sombra
- Formas de VML, elemento Shadow
- Linguagem VML (VML), desenho com efeitos de sombra
- VML (linguagem VML), desenho com efeitos de sombra
- gráficos vetoriais, desenho com efeitos de sombra
- Formas de VML, desenho com efeitos de sombra
- desenho com efeitos de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83be3f59eacfb495a2c80d212bc99cfd3d43be10aa8144eb68d3defd8a029e41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512587"
---
# <a name="using-the-shadow-element"></a>Usando o elemento Shadow

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Neste tópico, Ilustraremos como usar o `<shadow>` subelemento para desenhar uma forma que tenha vários efeitos de sombra.

Você pode posicionar o `<shadow>` subelemento dentro do `<shape>` , `<shapetype>` ou qualquer elemento Shape predefinido para desenhar uma forma com uma sombra. Você pode usar os atributos de Propriedade do `<shadow>` subelemento para personalizar a sombra.

Por exemplo, para criar uma forma com uma sombra, conforme mostrado na imagem a seguir, você pode digitar as seguintes linhas na `<BODY>` região da sua página da Web:

![shape1.gif (887 bytes)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` e `type="perspective"` indique ativar a sombra usando o tipo de perspectiva.
-   A **origem** e o **deslocamento** indicam onde desenhar a sombra.
-   `matrix="..."` Especifica a matriz de transformação de perspectiva.

Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .

 

 