---
title: Agrupando formas
description: Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Web Workshop, agrupando formas
- Criando páginas da Web, agrupando formas
- Linguagem VML (VML), agrupamento de formas
- VML (linguagem VML), agrupamento de formas
- gráficos vetoriais, agrupamento de formas
- Formas de VML, agrupamento
- agrupando formas
- Linguagem VML (VML), elemento de grupo
- VML (linguagem VML), elemento de grupo
- gráficos vetoriais, elemento Group
- elemento de grupo
- Elementos de VML, grupo
- Linguagem VML (VML), espaço de coordenadas local
- VML (linguagem VML), espaço de coordenadas local
- gráficos vetoriais, espaço de coordenadas local
- espaço de coordenadas local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008066"
---
# <a name="grouping-shapes"></a>Agrupando formas

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Como você aprendeu, você pode facilmente desenhar formas individuais usando VML. Nesta seção, explicaremos os benefícios do agrupamento de formas e como agrupar formas.

Se você tivesse muitas formas que precisavam ser dimensionadas, movidas ou giradas juntas, você acharia entediante definir os atributos individualmente para cada forma. Além disso, você aumentaria a margem de erros. Seria melhor se você pudesse agrupar as formas e, em seguida, definir os atributos de todo o grupo.

Na VML, você pode usar o `<group>` elemento para agrupar muitas formas para que elas possam ser transformadas como uma unidade. Por exemplo, conforme mostrado na representação de VML a seguir, você pode facilmente agrupar duas formas.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Quando as formas são agrupadas, elas usam o [espaço de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) do grupo. Portanto, as formas dentro de um grupo podem ser dimensionadas e movidas juntas. Você verá mais exemplos no tópico usar espaço de coordenadas local.

Dentro de um grupo, você pode ter quantas formas ou grupos desejar. Quando um grupo está dentro de outro grupo, ele é chamado de "grupo aninhado". Não há nenhuma limitação nos níveis de aninhamento.

Por exemplo, as linhas a seguir demonstram um grupo aninhado de 3 níveis. Shape3 e Shape4 estão em GroupC. Shape2 e GroupC estão em GroupB. Shape1 e GroupB estão no GroupA.


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .

[![voltar ao início ](images/top.gif) para cima](#top)

## <a name="summary"></a>Resumo

Você pode usar o `<group>` elemento para agrupar muitas formas para que elas possam ser transformadas como uma unidade.

 

 