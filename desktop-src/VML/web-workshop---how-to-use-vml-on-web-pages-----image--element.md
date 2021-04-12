---
title: Usando o elemento Image
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web Workshop, elemento Image
- Criando páginas da Web, elemento Image
- Linguagem VML (VML), elemento Image
- VML (linguagem VML), elemento Image
- gráficos vetoriais, elemento Image
- elemento de imagem
- Elementos de VML, imagem
- Formas de VML, elemento Image
- Linguagem VML (VML), atributos de propriedade de corte
- VML (linguagem VML), atributos de propriedade de corte
- gráficos vetoriais, atributos de propriedade de corte
- Formas de VML, atributos de propriedade de corte
- cortar atributos de propriedade
- Linguagem VML (VML), obter atributo de propriedade
- VML (linguagem VML), obter atributo de propriedade
- gráfico vetorial, obter atributo de propriedade
- Formas de VML, obter atributo de propriedade
- obter atributo de propriedade
- Linguagem VML (VML), contraste
- VML (linguagem VML), contraste
- gráficos vetoriais, contraste
- Formas de VML, contraste
- Linguagem VML (VML), atributo de propriedade blacklevel
- VML (linguagem VML), atributo de propriedade blacklevel
- gráficos vetoriais, atributo de propriedade blacklevel
- Formas de VML, atributo de propriedade blacklevel
- atributo de propriedade blacklevel
- Linguagem VML (VML), brilho
- VML (linguagem VML), brilho
- gráficos vetoriais, brilho
- Formas de VML, brilho
- Linguagem VML (VML), atributo de propriedade de escala de cinza
- VML (linguagem VML), atributo de propriedade de escala de cinza
- gráficos vetoriais, atributo de propriedade tons de cinza
- Formas de VML, atributo de propriedade de escala de cinza
- atributo de propriedade de escala de cinza
- Linguagem VML (VML), atributo de propriedade gama
- VML (linguagem VML), atributo de propriedade gama
- gráficos vetoriais, atributo de propriedade gama
- Formas de VML, atributo de propriedade gama
- atributo de propriedade gama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499131"
---
# <a name="using-the-image-element"></a>Usando o elemento Image

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Usando `<image>`

Neste tópico, Ilustraremos como usar o `<image>` elemento para exibir imagens com vários efeitos especiais.

Se você quisesse exibir uma imagem que foi carregada a partir de uma fonte externa, normalmente usaria o `<img>` elemento fornecido em HTML e, em seguida, apontaria o atributo de propriedade **src** para o local do arquivo de imagem.

Como alternativa, você pode usar o `<image>` elemento fornecido em VML. Ao usar o `<image>` elemento, você pode criar apenas um arquivo de imagem e, em seguida, exibir a imagem de maneira diferente alterando os atributos de Propriedade do `<image>` elemento. Além disso, `<image>` o elemento fornece vários efeitos especiais que você não pode fazer simplesmente usando o `<img>` elemento de HTML, como [corte](#crop), [contraste](#contrast), [brilho](#brightness), [gama](#gamma)e [escala de cinza](#grayscale).

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="crop"></a>cortar

Você pode usar os atributos de propriedade **cropbottom**, **croptop**, **CropLeft** e **CropRight** do `<image>` elemento para exibir imagens diferentes que são cortadas do mesmo arquivo de imagem.

O valor desses atributos de corte representa a porcentagem de recorte da borda da imagem. O valor pode ser qualquer número entre 0 e 1. Por padrão, o valor é definido como 0, indicando que não há nenhum corte na borda. O valor 0,1 indica um corte de 10 por cento da borda, o valor 0,15 indica um corte de 15 por cento a partir da borda e assim por diante.

Por exemplo, para exibir cinco imagens que são todas cortadas do mesmo arquivo de imagem, você pode usar o `<image>` elemento e especificar valores de corte diferentes, conforme mostrado na seguinte representação de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image1 (1969 bytes)](images/image1-2.jpg)![\-3.jpg image1 (1148 bytes)](images/image1-3.jpg)![\-4.jpg image1 (1686 bytes)](images/image1-4.jpg)![\-5.jpg image1 (1364 bytes)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





A primeira imagem, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , não tem nenhum valor de corte. Portanto, 100% da imagem original é exibido em um tamanho de 100 pontos por 80 pontos.

A segunda imagem, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , tem alguns valores de corte. `cropbottom="0.2"` indica que 20 por cento da imagem serão cortados da parte inferior; `cropright="0.15"` indica que 15 por cento da imagem será cortado da borda direita. A imagem restante é exibida em um tamanho de 85 pontos por 64 pontos.

Da mesma forma, a terceira, a quarta e a quinta imagens têm alguns valores de corte. A imagem original é cortada de acordo com os valores de corte e, em seguida, é exibida de acordo com o valor de largura e altura.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="contrast"></a>contraste

Você pode usar o atributo **obter** Propriedade do `<image>` elemento para exibir várias imagens que têm configurações de contraste diferentes.

O valor do atributo de propriedade de **obter** pode ser qualquer número. Por padrão, o valor é 1, indicando o uso do mesmo contraste da imagem original. O valor 0 indica sem contraste. Quanto maior o número, maior o contraste.

Por exemplo, para exibir cinco imagens que têm configurações de contraste diferentes, você pode usar o `<image>` elemento e definir um valor diferente para o atributo de propriedade de **obter** , conforme mostrado na seguinte representação de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image2 (270 bytes)](images/image2-2.jpg)![\-3.jpg image2 (1919 bytes)](images/image2-3.jpg)![\-4.jpg image2 (3143 bytes)](images/image2-4.jpg)![\-5.jpg image2 (1724 bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Quando o atributo de propriedade de **obter** é definido como 0, a imagem inteira torna-se cinza porque não há contraste. O contraste é mais perceptível quando o atributo de propriedade de **obter** é definido como 3 do que quando é definido como 0,5. O contraste é invertido quando o atributo de propriedade de **obter** é definido como um valor negativo como-0,4.

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="brightness"></a>lo

Você pode usar o atributo de propriedade **blacklevel** do `<image>` elemento para exibir várias imagens que têm configurações de brilho diferentes.

O valor do atributo da propriedade **blacklevel** pode ser qualquer valor entre 0 e 1. Por padrão, o valor é 0, indicando que o nível de brilho na imagem original é preservado. O valor 1 indica o nível mais alto de brilho.

Por exemplo, para exibir cinco imagens que têm configurações de brilho diferentes, você pode usar o `<image>` elemento e definir um valor diferente para o atributo de propriedade **blacklevel** , conforme mostrado na seguinte representação de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image3 (2579 bytes)](images/image3-2.jpg)![\-3.jpg image3 (2330 bytes)](images/image3-3.jpg)![\-4.jpg image3 (2727 bytes)](images/image3-4.jpg)![\-5.jpg image3 (2435 bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="grayscale"></a>escala de cinza

Você pode usar o atributo de propriedade de **escala de cinza** do `<image>` elemento para exibir imagens com ou sem tons de cinza.

O valor do atributo da propriedade de **escala de cinza** pode ser true ou false. Por padrão, o valor é definido como false para que a imagem seja exibida em cores. Se o valor for definido como true, a imagem será exibida em escala de cinza.

Por exemplo, conforme mostrado na imagem a seguir, a primeira imagem usa a configuração padrão (false) do atributo de escala de cinza ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Portanto, a imagem é exibida em cores.

A segunda imagem define o atributo de escala de cinza como true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ). Portanto, a imagem é exibida em escala de cinza, conforme mostrado na seguinte representação de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![\-2.jpg image4 (2138 bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="gamma"></a>gamma

Você pode usar o atributo de propriedade **gama** do `<image>` elemento para exibir imagens que têm diferentes configurações de gama.

O valor do atributo de propriedade gama pode ser qualquer valor entre 0 e 1. Por padrão, o valor é definido como 1.

Por exemplo, para exibir três imagens que têm diferentes configurações de gama, você pode usar o `<image>` elemento e definir um valor diferente do atributo de propriedade **gama** , conforme mostrado na seguinte representação de VML:

![\-1.jpg image5 (2714 bytes)](images/image5-1.jpg)![\-2.jpg image5 (2729 bytes)](images/image5-2.jpg)![\-3.jpg image5 (2726 bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 