---
description: 'Ao implementar seu próprio reconhecedor de gestos da Microsoft, você deve definir o nome e o valor de intervalo Unicode para qualquer gesto que seu reconhecedor reconheça. Se você decidir implementar os gestos que já têm suporte ou estiverem definidos como parte do reconhecedor de gestos da Microsoft, use os nomes definidos e valores de intervalo Unicode para esses gestos. A coleção inteira de nomes e valores de intervalo Unicode para gestos implementados e não implementados no reconhecedor de gestos da Microsoft são fornecidas no arquivo de cabeçalho Recdefs. h (instalado por padrão em C: \\ arquivos de programas \\ Microsoft Tablet PC Platform SDK \\ incluem). Os nomes dos gestos e os valores de intervalo Unicode também estão listados nas tabelas a seguir. Observe que o \_ gesto nulo do gesto é usado para indicar que um reconhecedor não reconhece a entrada como um gesto.'
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Valores de intervalo Unicode de gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b66b9b4ee511e9eeadd79e0dff2675391ceee6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797681"
---
# <a name="unicode-range-values-of-gestures"></a>Valores de intervalo Unicode de gestos

Ao implementar seu próprio reconhecedor de gestos da Microsoft, você deve definir o nome e o valor de intervalo Unicode para qualquer gesto que seu reconhecedor reconheça.

Se você decidir implementar os gestos que já têm suporte ou estiverem definidos como parte do reconhecedor de gestos da Microsoft, use os nomes definidos e valores de intervalo Unicode para esses gestos. A coleção inteira de nomes e valores de intervalo Unicode para gestos implementados e não implementados no reconhecedor de gestos da Microsoft são fornecidas no arquivo de cabeçalho Recdefs. h (instalado por padrão em C: \\ arquivos de programas \\ Microsoft Tablet PC Platform SDK \\ incluem). Os nomes dos gestos e os valores de intervalo Unicode também estão listados nas tabelas a seguir.

> [!Note]  
> O gesto de gesto \_ nulo é usado para indicar que um reconhecedor não reconhece a entrada como um gesto.

 

## <a name="implemented-gestures"></a>Gestos implementados



| Nome do gesto                          | Valor de intervalo Unicode |
|---------------------------------------|---------------------|
| GESTO \_ nulo<br/>              | 0xf000<br/>   |
| \_riscar gestos<br/>        | 0xf001<br/>   |
| triângulo do gesto \_<br/>          | 0xf002<br/>   |
| quadrado de gesto \_<br/>            | 0xf003<br/>   |
| estrela do gesto \_<br/>              | 0xf004<br/>   |
| verificação de gesto \_<br/>             | 0xf005<br/>   |
| CURLICUE do gesto \_<br/>          | 0xf010<br/>   |
| \_CURLICUE dupla de gesto \_<br/>  | 0xf011<br/>   |
| círculo do gesto \_<br/>            | 0xf020<br/>   |
| \_círculo duplo de gesto \_<br/>    | 0xf021<br/>   |
| \_semicírculo \_ esquerdo do gesto<br/>  | 0xf028<br/>   |
| GESTO em \_ semicírculo \_ à direita<br/> | 0xf029<br/>   |
| \_divisa \_ para cima<br/>       | 0xf030<br/>   |
| divisa de gesto \_ \_ para baixo<br/>     | 0xf031<br/>   |
| \_divisa \_ esquerda do gesto<br/>     | 0xf032<br/>   |
| \_divisa \_ direita<br/>    | 0xf033<br/>   |
| seta do gesto para \_ \_ cima<br/>         | 0xf038<br/>   |
| seta do gesto \_ \_ para baixo<br/>       | 0xf039<br/>   |
| seta de gesto \_ para a \_ esquerda<br/>       | 0xf03a<br/>   |
| \_seta para o gesto \_ à direita<br/>      | 0xf03b<br/>   |
| GESTO \_ para cima<br/>                | 0xf058<br/>   |
| GESTO \_ para baixo<br/>              | 0xf059<br/>   |
| restante do gesto \_<br/>              | 0xf05a<br/>   |
| direito de gesto \_<br/>             | 0xf05b<br/>   |
| GESTO \_ \_ para cima<br/>          | 0xf060<br/>   |
| GESTO \_ para baixo \_<br/>          | 0xf061<br/>   |
| GESTO para a \_ esquerda à \_ direita<br/>       | 0xf062<br/>   |
| GESTO \_ \_ à direita à esquerda<br/>       | 0xf063<br/>   |
| GESTO \_ para cima para cima \_ à esquerda \_<br/>    | 0xf064<br/>   |
| GESTO \_ para cima \_ à direita \_<br/>   | 0xf065<br/>   |
| GESTO \_ para baixo \_ esquerdo \_ longo<br/>  | 0xf066<br/>   |
| GESTO \_ para baixo \_ à direita \_<br/> | 0xf067<br/>   |
| GESTO \_ para cima \_ à esquerda<br/>          | 0xf068<br/>   |
| GESTO \_ para cima \_ à direita<br/>         | 0xf069<br/>   |
| GESTO \_ para baixo \_ à esquerda<br/>        | 0xf06a<br/>   |
| GESTO \_ para baixo \_ à direita<br/>       | 0xf06b<br/>   |
| GESTO \_ esquerdo \_ para cima<br/>          | 0xf06c<br/>   |
| GESTO \_ esquerdo \_ para baixo<br/>        | 0xf06d<br/>   |
| GESTO \_ \_ de direita para cima<br/>         | 0xf06e<br/>   |
| GESTO \_ direito \_ para baixo<br/>       | 0xf06f<br/>   |
| \_exclamação do gesto<br/>       | 0xf0a4<br/>   |
| toque do gesto \_<br/>               | 0xf0f0<br/>   |
| \_toque duplo de gesto \_<br/>       | 0xf0f1<br/>   |



 

## <a name="unimplemented-gestures"></a>Gestos não implementados



| Nome do gesto                             | Valor de intervalo Unicode |
|------------------------------------------|---------------------|
| infinito de gesto \_<br/>             | 0xf006<br/>   |
| Cruz do gesto \_<br/>                | 0xf007<br/>   |
| parágrafo do gesto \_<br/>            | 0xf008<br/>   |
| seção de GESTOs \_<br/>              | 0xf009<br/>   |
| marcador de gesto \_<br/>               | 0xf00a<br/>   |
| \_item \_ cruzado do gesto<br/>        | 0xf00b<br/>   |
| Rabisco do gesto \_<br/>             | 0xf00c<br/>   |
| troca de GESTOs \_<br/>                 | 0xf00d<br/>   |
| OPENUP do gesto \_<br/>               | 0xf00e<br/>   |
| CLOSEUP do gesto \_<br/>              | 0xf00f<br/>   |
| retângulo do gesto \_<br/>            | 0xf012<br/>   |
| \_toque de círculo do gesto \_<br/>          | 0xf022<br/>   |
| \_círculo do círculo do gesto \_<br/>       | 0xf023<br/>   |
| \_Cruz do círculo do gesto \_<br/>        | 0xf025<br/>   |
| linha do círculo do gesto \_ \_ \_ vertical<br/>   | 0xf026<br/>   |
| linha de círculo do gesto \_ \_ \_ na horizontal<br/>   | 0xf027<br/>   |
| \_seta dupla \_ \_ de gesto para cima<br/>    | 0xf03c<br/>   |
| \_seta dupla de gesto \_ \_ para baixo<br/>  | 0xf03d<br/>   |
| \_seta dupla \_ \_ à esquerda do gesto<br/>  | 0xf03e<br/>   |
| \_seta dupla \_ \_ à direita do gesto<br/> | 0xf03f<br/>   |
| seta para cima do gesto \_ \_ \_ à esquerda<br/>      | 0xf040<br/>   |
| \_seta para \_ cima \_ direita do gesto<br/>     | 0xf041<br/>   |
| \_seta para baixo do gesto \_ \_ à esquerda<br/>    | 0xf042<br/>   |
| \_seta para \_ baixo \_ do gesto à direita<br/>   | 0xf043<br/>   |
| \_seta para a esquerda do gesto \_ \_ para cima<br/>      | 0xf044<br/>   |
| seta para a esquerda do gesto \_ \_ \_ para baixo<br/>    | 0xf045<br/>   |
| \_seta para a direita do gesto \_ \_ para cima<br/>     | 0xf046<br/>   |
| \_seta para a direita do gesto \_ \_ para baixo<br/>   | 0xf047<br/>   |
| \_LEFTUP diagonal de gesto \_<br/>     | 0xf05c<br/>   |
| \_RIGHTUP diagonal de gesto \_<br/>    | 0xf05d<br/>   |
| \_LEFTDOWN diagonal de gesto \_<br/>   | 0xf05e<br/>   |
| \_RIGHTDOWN diagonal de gesto \_<br/>  | 0xf05f<br/>   |
| \_letra \_ de gesto A<br/>            | 0xf080<br/>   |
| letra do gesto \_ \_ B<br/>            | 0xf081<br/>   |
| letra do gesto \_ \_ C<br/>            | 0xf082<br/>   |
| letra do gesto \_ \_ D<br/>            | 0xf083<br/>   |
| letra do gesto \_ \_ E<br/>            | 0xf084<br/>   |
| letra do gesto \_ \_ F<br/>            | 0xf085<br/>   |
| letra do gesto \_ \_ G<br/>            | 0xf086<br/>   |
| letra do gesto \_ \_ H<br/>            | 0xf087<br/>   |
| letra do gesto \_ \_ I<br/>            | 0xf088<br/>   |
| letra do gesto \_ \_ J<br/>            | 0xf089<br/>   |
| letra do gesto \_ \_ K<br/>            | 0xf08a<br/>   |
| letra do gesto \_ \_ L<br/>            | 0xf08b<br/>   |
| letra do gesto \_ \_ M<br/>            | 0xf08c<br/>   |
| letra do gesto \_ \_ N<br/>            | 0xf08d<br/>   |
| letra do gesto \_ \_ O<br/>            | 0xf08e<br/>   |
| letra do gesto \_ \_ P<br/>            | 0xf08f<br/>   |
| letra do gesto \_ \_ Q<br/>            | 0xf090<br/>   |
| letra do gesto \_ \_ R<br/>            | 0xf091<br/>   |
| letra do gesto \_ \_ S<br/>            | 0xf092<br/>   |
| letra do gesto \_ \_ T<br/>            | 0xf093<br/>   |
| letra do gesto \_ \_ U<br/>            | 0xf094<br/>   |
| letra do gesto \_ \_ V<br/>            | 0xf095<br/>   |
| letra do gesto \_ \_ W<br/>            | 0xf096<br/>   |
| letra do gesto \_ \_ X<br/>            | 0xf097<br/>   |
| letra do gesto \_ \_ Y<br/>            | 0xf098<br/>   |
| letra do gesto \_ \_ Z<br/>            | 0xf099<br/>   |
| \_Dígito \_ 0 do gesto<br/>             | 0xf09a<br/>   |
| \_Dígito \_ 1 do gesto<br/>             | 0xf09b<br/>   |
| \_Dígito \_ 2 do gesto<br/>             | 0xf09c<br/>   |
| \_Dígito \_ 3 do gesto<br/>             | 0xf09d<br/>   |
| \_Dígito \_ 4 do gesto<br/>             | 0xf09e<br/>   |
| \_Dígito \_ 5 do gesto<br/>             | 0xf09f<br/>   |
| \_Dígito \_ 6 do gesto<br/>             | 0xf0a0<br/>   |
| \_Dígito \_ 7 do gesto<br/>             | 0xf0a1<br/>   |
| \_Dígito \_ 8 do gesto<br/>             | 0xf0a2<br/>   |
| \_Dígito \_ 9 do gesto<br/>             | 0xf0a3<br/>   |
| pergunta do gesto \_<br/>             | 0xf0a5<br/>   |
| nítido do gesto \_<br/>                | 0xf0a6<br/>   |
| Dólar do gesto \_<br/>               | 0xf0a7<br/>   |
| asterisco do gesto \_<br/>             | 0xf0a8<br/>   |
| GESTO \_ mais<br/>                 | 0xf0a9<br/>   |
| \_dobrar gesto \_ para cima<br/>           | 0xf0b8<br/>   |
| \_dobra dupla do gesto \_<br/>         | 0xf0b9<br/>   |
| \_dupla \_ à esquerda do gesto<br/>         | 0xf0ba<br/>   |
| \_dupla \_ à direita do gesto<br/>        | 0xf0bb<br/>   |
| GESTO \_ triplo \_ para cima<br/>           | 0xf0bc<br/>   |
| GESTO \_ triplo \_ para baixo<br/>         | 0xf0bd<br/>   |
| GESTO \_ triplo \_ à esquerda<br/>         | 0xf0be<br/>   |
| GESTO \_ triplo \_ direito<br/>        | 0xf0bf<br/>   |
| colchete de gesto \_ \_<br/>        | 0xf0e4<br/>   |
| colchete de gesto \_ \_ em<br/>       | 0xf0e5<br/>   |
| \_colchete \_ esquerdo do gesto<br/>        | 0xf0e6<br/>   |
| \_colchete \_ direito do gesto<br/>       | 0xf0e7<br/>   |
| chave do gesto \_ \_ sobre<br/>          | 0xf0e8<br/>   |
| chave do gesto \_ \_ em<br/>         | 0xf0e9<br/>   |
| chave do gesto \_ \_ à esquerda<br/>          | 0xf0ea<br/>   |
| \_chave \_ do gesto à direita<br/>         | 0xf0eb<br/>   |
| \_toque triplo do gesto \_<br/>          | 0xf0f2<br/>   |
| \_toque Quad do gesto \_<br/>            | 0xf0f3<br/>   |



 

 

 




