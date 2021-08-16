---
description: 'Ao implementar seu próprio reconhecedor de gestos da Microsoft, você deve definir o nome e o valor do intervalo Unicode para qualquer gesto que o reconhecedor reconheça. Se você decidir implementar os gestos que já têm suporte ou definidos como parte do reconhecedor de gestos da Microsoft, use os nomes definidos e os valores de intervalo Unicode para esses gestos. Toda a coleção de nomes e valores de intervalo Unicode para gestos implementados e não implementados no reconhecedor de gestos da Microsoft é fornecida no arquivo de header Recdefs.h (instalado por padrão em C: Arquivos de Programas Microsoft \\ \\ Tablet PC Platform SDK \\ Include). Os nomes de gesto e os valores de intervalo Unicode também são listados nas tabelas a seguir. Observação O gesto GESTURE \_ NULL é usado para indicar que um reconhecedor não reconhece a entrada como um gesto.'
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Valores de intervalo Unicode de gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f96c1f59ea9e53d63999c01db73c45080f205bccf043e26463563b0f1f6af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449219"
---
# <a name="unicode-range-values-of-gestures"></a>Valores de intervalo Unicode de gestos

Ao implementar seu próprio reconhecedor de gestos da Microsoft, você deve definir o nome e o valor do intervalo Unicode para qualquer gesto que o reconhecedor reconheça.

Se você decidir implementar os gestos que já têm suporte ou definidos como parte do reconhecedor de gestos da Microsoft, use os nomes definidos e os valores de intervalo Unicode para esses gestos. Toda a coleção de nomes e valores de intervalo Unicode para gestos implementados e não implementados no reconhecedor de gestos da Microsoft é fornecida no arquivo de header Recdefs.h (instalado por padrão em C: Arquivos de Programas Microsoft \\ \\ Tablet PC Platform SDK \\ Include). Os nomes de gesto e os valores de intervalo Unicode também são listados nas tabelas a seguir.

> [!Note]  
> O gesto GESTURE \_ NULL é usado para indicar que um reconhecedor não reconhece a entrada como um gesto.

 

## <a name="implemented-gestures"></a>Gestos implementados



| Nome do gesto                          | Valor do intervalo Unicode |
|---------------------------------------|---------------------|
| GESTO \_ NULO<br/>              | 0xf000<br/>   |
| RASCUNHO \_ DE GESTO<br/>        | 0xf001<br/>   |
| TRIÂNGULO \_ DE GESTO<br/>          | 0xf002<br/>   |
| QUADRADO DE \_ GESTOS<br/>            | 0xf003<br/>   |
| ESTRELA DE \_ GESTO<br/>              | 0xf004<br/>   |
| VERIFICAÇÃO DE \_ GESTO<br/>             | 0xf005<br/>   |
| \_CURLICUE DE GESTO<br/>          | 0xf010<br/>   |
| \_ \_ CURLICUE DUPLA DE GESTOS<br/>  | 0xf011<br/>   |
| CÍRCULO DE \_ GESTOS<br/>            | 0xf020<br/>   |
| CÍRCULO \_ DUPLO \_ DE GESTOS<br/>    | 0xf021<br/>   |
| GESTO \_ SEMICIRCLEO \_ À ESQUERDA<br/>  | 0xf028<br/>   |
| GESTO \_ SEMICIRCLE \_ À DIREITA<br/> | 0xf029<br/>   |
| DIVISA \_ DE GESTO PARA \_ CIMA<br/>       | 0xf030<br/>   |
| DIVISA \_ DE GESTO PARA \_ BAIXO<br/>     | 0xf031<br/>   |
| DIVISA \_ DE GESTO À \_ ESQUERDA<br/>     | 0xf032<br/>   |
| DIVISA \_ DE GESTO À \_ DIREITA<br/>    | 0xf033<br/>   |
| SETA \_ DE GESTO \_ PARA CIMA<br/>         | 0xf038<br/>   |
| SETA \_ DE GESTO \_ PARA BAIXO<br/>       | 0xf039<br/>   |
| SETA \_ DE GESTO PARA A \_ ESQUERDA<br/>       | 0xf03a<br/>   |
| SETA \_ DE GESTO PARA A \_ DIREITA<br/>      | 0xf03b<br/>   |
| GESTO \_ PARA CIMA<br/>                | 0xf058<br/>   |
| GESTO \_ PARA BAIXO<br/>              | 0xf059<br/>   |
| GESTO \_ À ESQUERDA<br/>              | 0xf05a<br/>   |
| GESTO \_ À DIREITA<br/>             | 0xf05b<br/>   |
| GESTO \_ PARA CIMA PARA \_ BAIXO<br/>          | 0xf060<br/>   |
| GESTO \_ PARA \_ BAIXO<br/>          | 0xf061<br/>   |
| GESTO \_ À ESQUERDA PARA A \_ DIREITA<br/>       | 0xf062<br/>   |
| GESTO \_ À ESQUERDA \_<br/>       | 0xf063<br/>   |
| GESTO \_ PARA CIMA À ESQUERDA POR MUITO \_ \_ TEMPO<br/>    | 0xf064<br/>   |
| GESTO \_ PARA CIMA POR MUITO \_ \_ TEMPO<br/>   | 0xf065<br/>   |
| GESTO \_ PARA BAIXO À ESQUERDA POR MUITO \_ \_ TEMPO<br/>  | 0xf066<br/>   |
| GESTO \_ PARA BAIXO PARA A DIREITA \_ \_ LONGO<br/> | 0xf067<br/>   |
| GESTO \_ PARA A \_ ESQUERDA<br/>          | 0xf068<br/>   |
| GESTO \_ PARA A \_ DIREITA<br/>         | 0xf069<br/>   |
| GESTO \_ PARA BAIXO À \_ ESQUERDA<br/>        | 0xf06a<br/>   |
| GESTO \_ PARA BAIXO PARA A \_ DIREITA<br/>       | 0xf06b<br/>   |
| GESTO \_ À \_ ESQUERDA<br/>          | 0xf06c<br/>   |
| GESTO \_ À ESQUERDA PARA \_ BAIXO<br/>        | 0xf06d<br/>   |
| GESTO \_ PARA \_ CIMA<br/>         | 0xf06e<br/>   |
| GESTO \_ PARA \_ BAIXO<br/>       | 0xf06f<br/>   |
| \_EXCLAMAÇÃO DE GESTO<br/>       | 0xf0a4<br/>   |
| TOQUE DE \_ GESTO<br/>               | 0xf0f0<br/>   |
| TOQUE \_ DUPLO \_ DE GESTO<br/>       | 0xf0f1<br/>   |



 

## <a name="unimplemented-gestures"></a>Gestos não simplificados



| Nome do gesto                             | Valor do intervalo Unicode |
|------------------------------------------|---------------------|
| INFINITO \_ DO GESTO<br/>             | 0xf006<br/>   |
| CRUZ DE \_ GESTO<br/>                | 0xf007<br/>   |
| PARÁGRAFO DE \_ GESTO<br/>            | 0xf008<br/>   |
| SEÇÃO \_ GESTO<br/>              | 0xf009<br/>   |
| MARCADOR DE \_ GESTO<br/>               | 0xf00a<br/>   |
| CRUZ \_ DE MARCADOR DE \_ GESTO<br/>        | 0xf00b<br/>   |
| \_ALTERNÂNCIA DE GESTOS<br/>             | 0xf00c<br/>   |
| TROCA DE \_ GESTOS<br/>                 | 0xf00d<br/>   |
| ABERTURA \_ DE GESTO<br/>               | 0xf00e<br/>   |
| CLOSEUP \_ DE GESTO<br/>              | 0xf00f<br/>   |
| RETÂNGULO \_ DE GESTO<br/>            | 0xf012<br/>   |
| TOQUE DE \_ CÍRCULO \_ DE GESTOS<br/>          | 0xf022<br/>   |
| CÍRCULO DE \_ CÍRCULO \_ DE GESTOS<br/>       | 0xf023<br/>   |
| CRUZ DE \_ CÍRCULO \_ DE GESTOS<br/>        | 0xf025<br/>   |
| VERT \_ DE LINHA DE CÍRCULO DE \_ \_ GESTO<br/>   | 0xf026<br/>   |
| GESTURE \_ CIRCLE \_ LINE \_ HORZ<br/>   | 0xf027<br/>   |
| GESTO DE \_ \_ SETA DUPLA \_ PARA CIMA<br/>    | 0xf03c<br/>   |
| GESTO DE \_ \_ SETA DUPLA \_ PARA BAIXO<br/>  | 0xf03d<br/>   |
| GESTO DE \_ \_ SETA DUPLA PARA \_ A ESQUERDA<br/>  | 0xf03e<br/>   |
| GESTO DE \_ \_ SETA DUPLA PARA \_ A DIREITA<br/> | 0xf03f<br/>   |
| GESTO PARA \_ CIMA \_ SETA PARA \_ A ESQUERDA<br/>      | 0xf040<br/>   |
| GESTO PARA \_ CIMA \_ SETA PARA \_ A DIREITA<br/>     | 0xf041<br/>   |
| GESTO PARA \_ BAIXO \_ SETA PARA \_ A ESQUERDA<br/>    | 0xf042<br/>   |
| GESTO PARA \_ BAIXO \_ SETA PARA \_ A DIREITA<br/>   | 0xf043<br/>   |
| SETA \_ PARA A ESQUERDA DO GESTO PARA \_ \_ CIMA<br/>      | 0xf044<br/>   |
| GESTO DE \_ \_ SETA PARA \_ BAIXO<br/>    | 0xf045<br/>   |
| GESTO \_ DE \_ SETA PARA A DIREITA PARA \_ CIMA<br/>     | 0xf046<br/>   |
| GESTO DE \_ \_ SETA PARA \_ A DIREITA PARA BAIXO<br/>   | 0xf047<br/>   |
| GESTO \_ DIAGONAL \_ LEFTUP<br/>     | 0xf05c<br/>   |
| GESTO \_ DIAGONAL PARA A \_ DIREITA<br/>    | 0xf05d<br/>   |
| GESTO \_ DIAGONAL \_ LEFTDOWN<br/>   | 0xf05e<br/>   |
| GESTO \_ DIAGONAL PARA A \_ DIREITA<br/>  | 0xf05f<br/>   |
| LETRA \_ DE GESTO \_ A<br/>            | 0xf080<br/>   |
| LETRA \_ DE GESTO \_ B<br/>            | 0xf081<br/>   |
| LETRA \_ DE GESTO \_ C<br/>            | 0xf082<br/>   |
| LETRA \_ DE GESTO \_ D<br/>            | 0xf083<br/>   |
| LETRA \_ DE GESTO \_ E<br/>            | 0xf084<br/>   |
| LETRA \_ DE GESTO \_ F<br/>            | 0xf085<br/>   |
| LETRA \_ DE GESTO \_ G<br/>            | 0xf086<br/>   |
| LETRA \_ DE GESTO \_ H<br/>            | 0xf087<br/>   |
| LETRA \_ DE \_ GESTO I<br/>            | 0xf088<br/>   |
| LETRA \_ DE GESTO \_ J<br/>            | 0xf089<br/>   |
| LETRA \_ DE GESTO \_ K<br/>            | 0xf08a<br/>   |
| LETRA \_ DE GESTO \_ L<br/>            | 0xf08b<br/>   |
| LETRA \_ DE GESTO \_ M<br/>            | 0xf08c<br/>   |
| LETRA \_ DE GESTO \_ N<br/>            | 0xf08d<br/>   |
| LETRA \_ DE GESTO \_ O<br/>            | 0xf08e<br/>   |
| LETRA \_ DE GESTO \_ P<br/>            | 0xf08f<br/>   |
| LETRA \_ DE GESTO \_ Q<br/>            | 0xf090<br/>   |
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



 

 

 




