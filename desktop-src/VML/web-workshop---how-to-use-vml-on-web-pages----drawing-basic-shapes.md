---
title: Desenhando formas básicas
description: Este artigo descreve o desenho de formas básicas no VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Workshop da Web, desenhando formas
- projetando páginas da Web, desenhando formas
- linguagem VML (VML), desenhando formas
- VML (linguagem VML), desenhando formas
- gráficos vetoriais, formas de desenho
- desenhando formas
- Formas de VML, desenho
- linguagem VML (VML), XML
- VML (linguagem VML),XML
- gráficos vetoriais, XML
- linguagem VML (VML), CSS2
- VML (linguagem VML),CSS2
- gráficos vetoriais, CSS2
- linguagem VML (VML), elementos
- VML (linguagem VML), elementos
- elementos gráficos vetoriais
- Elementos VML, formas de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00701e8ac77bd5bda7156c04ca25427d131646bf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407729"
---
# <a name="drawing-basic-shapes"></a>Desenhando formas básicas

Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Neste tópico, ilustramos como é fácil desenhar uma forma usando o VML.

Para criar uma oval vermelha em uma página da Web, conforme mostrado na figura a seguir, você pode desenhar a oval usando uma ferramenta de edição gráfica, salvar o desenho como um bitmap e inserir o bitmap na página da Web:

![oval1.gif (627 bytes)](images/oval1.gif)

Como alternativa, você pode usar o VML para desenhar gráficos. No exemplo anterior, você pode digitar as seguintes linhas na região da `<BODY>` página da Web para desenhar a oval vermelha:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` e `</v:...>` são a marca de início e a marca de término na sintaxe [XML](#xml-structure).`style='width:100pt; height:75pt'` fornece [informações css](#css-information). **oval** e **fillcolor**="red" são [elementos VML](#vml-elements).

Você pode alterar os gráficos simplesmente alterando seus atributos de propriedade no VML. No exemplo anterior, se você alterar para , conforme mostrado na seguinte representação de VML, a oval vermelha `fillcolor="red"` mudará para `fillcolor="blue"` azul:


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





Navegadores que suportam VML podem renderizar e exibir os gráficos representados no VML sem precisar baixar arquivos de imagem separados. A maioria dos gráficos representados no VML é renderizada mais rapidamente em navegadores e exige menos espaço em disco e tempo de download.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="xml-structure"></a>Estrutura XML

O VML é formatado de acordo com as regras de linguagem XML (XML). Qualquer analisador XML padrão pode analisar o VML e entregar os dados resultantes para um processador específico do VML. Para permitir que os navegadores saibam como entregar dados para um processador específico do VML, você precisa digitar algumas informações, como [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) e [objetos personalizados inseridos.](web-workshop---how-to-use-vml-on-web-pages----appendix.md) Em seguida, você pode usar o VML para digitar gráficos na região, assim como `<BODY>` fez no exemplo anterior.

O `"v:"` prefixo em cada marca XML identifica a marca como VML. O `"v:"` prefixo na `<BODY>` região deve ser consistente com `<html xmlns:v="...">` .

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="css-information"></a>Informações de CSS

O VML [usa folhas de estilos em cascata, Nível 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) para determinar o tamanho dos gráficos e posicionar os gráficos em uma página da Web. No exemplo anterior, especificamos o tamanho da oval como 100 pontos (largura) em 75 pontos (altura) ( `style='width:100pt;height:75pt'` ).

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="vml-elements"></a>Elementos VML

No exemplo anterior, utilizamos um elemento predefinido de VML `<oval>` para desenhar uma oval. Em seguida, utilizamos o atributo de propriedade **fillcolor** `<oval>` do elemento para preencher a oval com vermelho.

Com base na seção Marcas de [início,](https://www.w3.org/TR/REC-xml#sec-starttags) marcas de extremidade e marcas Empty-Element da especificação [XML 1.0](https://www.w3.org/TR/REC-xml), as marcas de elemento vazio podem ser usadas para qualquer elemento que não tenha conteúdo. Por exemplo, conforme mostrado na representação VML a seguir, não há nenhum conteúdo (sub-elemento) dentro do `<oval>` elemento . (Observe que o **estilo e** **fillcolor** são os atributos do `<oval>` elemento; eles não são sub-elementos.)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



Portanto, você pode usar a marca de elemento vazio, conforme mostrado na representação VML a seguir, para representar a mesma coisa que a linha acima.


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="summary"></a>Resumo

Você pode usar o VML para desenhar gráficos em uma página da Web e, em seguida, personalizar esses gráficos simplesmente alterando seus atributos de propriedade. Além disso, a maioria dos gráficos representados no VML é renderizada mais rapidamente em navegadores e leva menos tempo de download e espaço em disco.

 

 