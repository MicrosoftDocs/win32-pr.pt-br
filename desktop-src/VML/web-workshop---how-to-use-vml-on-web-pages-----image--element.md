---
title: Usando o elemento Image
description: Este artigo descreve o uso do elemento Image no VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Workshop da Web, elemento image
- projetando páginas da Web, elemento image
- linguagem VML (VML), elemento image
- VML (linguagem VML), elemento image
- gráficos vetoriais, elemento image
- elemento de imagem
- Elementos VML, imagem
- Formas VML, elemento image
- linguagem VML (VML), atributos de propriedade de corte
- VML (linguagem VML), atributos de propriedade de corte
- gráficos vetoriais, atributos de propriedade de corte
- Formas VML, atributos de propriedade de corte
- atributos de propriedade crop
- linguagem VML (VML), obter atributo de propriedade
- VML (linguagem VML), atributo de propriedade gain
- gráficos vetoriais, atributo de propriedade gain
- Formas VML, atributo de propriedade gain
- atributo de propriedade gain
- linguagem VML (VML), contraste
- VML (linguagem VML),contraste
- gráficos vetoriais, contraste
- Formas VML, contraste
- linguagem VML (VML), atributo de propriedade blacklevel
- VML (linguagem VML), atributo de propriedade blacklevel
- gráficos vetoriais, atributo de propriedade blacklevel
- Formas VML, atributo de propriedade blacklevel
- Atributo de propriedade blacklevel
- linguagem VML (VML), brilho
- VML (linguagem VML), brilho
- gráficos vetoriais, brilho
- Formas VML, brilho
- linguagem VML (VML), atributo de propriedade grayscale
- VML (linguagem VML), atributo de propriedade grayscale
- gráficos vetoriais, atributo de propriedade grayscale
- Formas VML, atributo de propriedade de escala de cinza
- atributo de propriedade grayscale
- linguagem VML (VML), atributo de propriedade gama
- VML (linguagem VML), atributo de propriedade gama
- gráficos vetoriais, atributo de propriedade gama
- Formas VML, atributo de propriedade gama
- Atributo de propriedade gama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407799"
---
# <a name="using-the-image-element"></a>Usando o elemento Image

Este tópico descreve o VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Usando `<image>`

Neste tópico, ilustramos como usar o elemento `<image>` para exibir imagens com vários efeitos especiais.

Se você quisesse exibir uma imagem carregada de uma fonte externa, normalmente usaria o elemento fornecido em HTML e, em seguida, apontaria o atributo de propriedade src para o local do arquivo `<img>` de imagem. 

Como alternativa, você pode usar o `<image>` elemento fornecido no VML. Ao usar o elemento , você pode criar apenas um arquivo de imagem e, em seguida, exibir a imagem de forma diferente alterando os atributos de `<image>` propriedade do `<image>` elemento. Além disso, o elemento fornece vários efeitos especiais que você não pode fazer simplesmente usando o elemento de HTML, como corte `<image>` `<img>` , contraste, brilho, [gama](#gamma) [](#crop) [](#contrast) [](#brightness)e escala de [cinza.](#grayscale)

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="crop"></a>cortar

Você pode usar os atributos de propriedade **cropbottom**, **croptop**, **cropleft** e **cropright** do elemento para exibir imagens diferentes que são cortadas do mesmo arquivo `<image>` de imagem.

O valor desses atributos de corte representa o corte percentual da borda da imagem. O valor pode ser qualquer número entre 0 e 1. Por padrão, o valor é definido como 0, indicando nenhuma recortação da borda. O valor 0,1 indica um corte de 10% da borda, o valor 0,15 indica um corte de 15% da borda e assim por diante.

Por exemplo, para exibir cinco imagens que são todas cortadas do mesmo arquivo de imagem, você pode usar o elemento e especificar valores de corte diferentes, conforme mostrado na seguinte representação `<image>` de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![image1 \-2.jpg (1969 bytes)](images/image1-2.jpg)![image1 \-3.jpg (1148 bytes)](images/image1-3.jpg)![image1 \-4.jpg (1686 bytes)](images/image1-4.jpg)![image1 \-5.jpg (1364 bytes)](images/image1-5.jpg)


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





A primeira imagem, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , não tem nenhum valor de corte. Portanto, 100% da imagem original é exibida em um tamanho de 100 pontos por 80 pontos.

A segunda imagem, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , tem alguns valores de corte. `cropbottom="0.2"` indica que 20% da imagem será cortada da parte inferior; `cropright="0.15"` indica que 15% da imagem será cortada da borda direita. A imagem restante é exibida em um tamanho de 85 pontos por 64 pontos.

Da mesma forma, a terceira, a quarta e a quinta imagens têm alguns valores de corte. A imagem original é cortada de acordo com os valores de corte e, em seguida, é exibida de acordo com o valor de largura e altura.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="contrast"></a>contraste

Você pode usar o **atributo de** propriedade gain do elemento para exibir várias imagens que `<image>` têm configurações de contraste diferentes.

O valor do **atributo de** propriedade gain pode ser qualquer número. Por padrão, o valor é 1, indicando o uso do mesmo contraste que a imagem original. O valor 0 não indica nenhum contraste. Quanto maior o número, maior o contraste.

Por exemplo, para exibir cinco imagens que têm configurações de contraste diferentes, você pode usar o elemento e definir um valor diferente para o atributo de propriedade gain, conforme mostrado na seguinte representação `<image>` de VML: 

![image1.jpg (5770 bytes)](images/image1.jpg)![image2 \-2.jpg (270 bytes)](images/image2-2.jpg)![image2 \-3.jpg (1919 bytes)](images/image2-3.jpg)![image2 \-4.jpg (3143 bytes)](images/image2-4.jpg)![image2 \-5.jpg (1724 bytes)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





Quando o **atributo de** propriedade gain é definido como 0, a imagem inteira fica cinza porque não há contraste. O contraste é mais perceptível quando o **atributo de** propriedade gain é definido como 3 do que quando ele é definido como 0,5. O contraste é invertido quando o **atributo de** propriedade gain é definido como um valor negativo, como -0,4.

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="brightness"></a>Brilho

Você pode usar o **atributo de propriedade de nível** preto do elemento para exibir várias imagens que têm `<image>` configurações de brilho diferentes.

O valor do atributo **de propriedade blacklevel** pode ser qualquer valor entre 0 e 1. Por padrão, o valor é 0, indicando que o nível de brilho na imagem original é preservado. O valor 1 indica o nível mais alto de brilho.

Por exemplo, para exibir cinco imagens que têm configurações de brilho diferentes, você pode usar o elemento e definir um valor diferente para o atributo de propriedade de nível preto, conforme mostrado na seguinte representação `<image>` de VML: 

![image1.jpg (5770 bytes)](images/image1.jpg)![image3 \-2.jpg (2579 bytes)](images/image3-2.jpg)![image3 \-3.jpg (2330 bytes)](images/image3-3.jpg)![image3 \-4.jpg (2727 bytes)](images/image3-4.jpg)![image3 \-5.jpg (2435 bytes)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="grayscale"></a>escala de cinza

Você pode usar o **atributo de propriedade grayscale** do `<image>` elemento para exibir imagens com ou sem escala de cinza.

O valor do atributo **de propriedade de escala** de cinza pode ser true ou false. Por padrão, o valor é definido como false para que a imagem seja exibida em cores. Se o valor for definido como true, a imagem será exibida em escala de cinza.

Por exemplo, conforme mostrado na imagem a seguir, a primeira imagem usa a configuração padrão (false)do atributo de escala de cinza ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ). Portanto, a imagem é exibida em cores.

A segunda imagem define o atributo de escala de cinza como true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ). Portanto, a imagem é exibida em escala de cinza, conforme mostrado na seguinte representação de VML:

![image1.jpg (5770 bytes)](images/image1.jpg)![image4 \-2.jpg (2138 bytes)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="gamma"></a>gamma

Você pode usar o atributo de propriedade **gama** do elemento `<image>` para exibir imagens que têm configurações gama diferentes.

O valor do atributo de propriedade gama pode ser qualquer valor entre 0 e 1. Por padrão, o valor é definido como 1.

Por exemplo, para exibir três imagens que têm configurações gama diferentes, você pode usar o elemento e definir um valor diferente do atributo de propriedade gama, conforme mostrado na seguinte representação `<image>` de VML: 

![image5 \-1.jpg (2714 bytes)](images/image5-1.jpg)![image5 \-2.jpg (2729 bytes)](images/image5-2.jpg)![image5 \-3.jpg (2726 bytes)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .

 

 