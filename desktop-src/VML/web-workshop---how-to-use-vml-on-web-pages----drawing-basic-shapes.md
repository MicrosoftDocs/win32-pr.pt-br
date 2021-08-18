---
title: Formas básicas de desenho
description: este artigo descreve o desenho de formas básicas em VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web Workshop, formas de desenho
- Criando páginas da Web, formas de desenho
- Linguagem VML (VML), desenhar formas
- VML (linguagem VML), formas de desenho
- gráficos vetoriais, formas de desenho
- desenhando formas
- Formas de VML, desenho
- Linguagem VML (VML), XML
- VML (linguagem VML), XML
- gráficos vetoriais, XML
- Linguagem VML (VML), CSS2
- VML (linguagem VML), CSS2
- gráficos vetoriais, CSS2
- Linguagem VML (VML), elementos
- VML (linguagem VML), elementos
- gráficos vetoriais, elementos
- Elementos de VML, formas de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4a8b7985371d9cffc6e7359cef1a17c69c403c7802de458b68d9df8c36e3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136919"
---
# <a name="drawing-basic-shapes"></a>Formas básicas de desenho

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Neste tópico, Ilustraremos como é fácil desenhar uma forma usando a VML.

Para criar uma elipse vermelha em uma página da Web, conforme mostrado na imagem a seguir, você pode desenhar a elipse usando uma ferramenta de edição gráfica, salvar o desenho como um bitmap e, em seguida, inserir o bitmap em sua página da Web:

![oval1.gif (627 bytes)](images/oval1.gif)

Como alternativa, você pode usar a VML para desenhar gráficos. No exemplo anterior, você pode digitar as seguintes linhas na `<BODY>` região da página da Web para desenhar a elipse vermelha:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` e `</v:...>` são a marca de início e a marca de fim na [sintaxe XML](#xml-structure).`style='width:100pt; height:75pt'` fornece [informações de CSS](#css-information). **oval** e **FillColor**= "vermelho" são [elementos de VML](#vml-elements).

Você pode alterar os elementos gráficos simplesmente alterando seus atributos de propriedade em VML. No exemplo anterior, se você alterar `fillcolor="red"` para `fillcolor="blue"` , conforme mostrado na representação de VML a seguir, a elipse vermelha será alterada para azul:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





Os navegadores que oferecem suporte a VML podem renderizar e exibir os gráficos representados em VML sem precisar baixar arquivos de imagem separados. A maioria dos gráficos representados em VML é renderizada mais rapidamente em navegadores e requer menos espaço em disco e tempo de download.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="xml-structure"></a>Estrutura XML

A VML é formatada de acordo com as regras de linguagem XML (XML). Qualquer analisador XML padrão pode analisar a VML e entregar os dados resultantes a um processador específico da VML. Para permitir que os navegadores saibam como entregar os dados a um processador específico da VML, você precisa digitar algumas informações, como [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) e [objetos personalizados incorporados](web-workshop---how-to-use-vml-on-web-pages----appendix.md). Em seguida, você pode usar a VML para digitar elementos gráficos na `<BODY>` região, assim como fazia no exemplo anterior.

O `"v:"` prefixo em cada marca XML identifica a marca como VML. O `"v:"` prefixo na `<BODY>` região deve ser consistente com `<html xmlns:v="...">` .

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="css-information"></a>Informações de CSS

A VML usa [folhas de estilos em cascata, nível 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) para determinar o tamanho dos gráficos e para posicionar os gráficos em uma página da Web. No exemplo anterior, especificamos o tamanho da oval como 100 pontos (largura) por 75 pontos (altura) ( `style='width:100pt;height:75pt'` ).

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="vml-elements"></a>Elementos VML

No exemplo anterior, usamos um elemento predefinido VML `<oval>` para desenhar uma oval. Em seguida, usamos o atributo da propriedade **FillColor** do `<oval>` elemento para preencher a oval com vermelho.

Com base nas [marcas de início, marcas de fim e Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) seção de marcas da [especificação XML 1,0](https://www.w3.org/TR/REC-xml), as marcas de elemento vazio podem ser usadas para qualquer elemento que não tenha conteúdo. Por exemplo, conforme mostrado na representação de VML a seguir, não há nenhum conteúdo (subelemento) dentro do `<oval>` elemento. (Observe que **Style** e **FillColor** são os atributos do `<oval>` elemento; eles não são subelementos.)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Portanto, você pode usar a marca de elemento vazio, conforme mostrado na representação de VML a seguir, para representar a mesma coisa que a linha acima.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="summary"></a>Resumo

Você pode usar a VML para desenhar gráficos em uma página da Web e, em seguida, personalizar esses gráficos simplesmente alterando seus atributos de propriedade. Além disso, a maioria dos gráficos representados em VML é renderizada mais rapidamente em navegadores e leva menos tempo para download e espaço em disco.

 

 