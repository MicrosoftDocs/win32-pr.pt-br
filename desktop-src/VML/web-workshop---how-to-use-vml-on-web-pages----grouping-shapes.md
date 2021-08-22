---
title: Agrupando formas
description: Este artigo descreve como agrupar formas no VML, um recurso que foi preterido a partir Windows Internet Explorer 9.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Workshop da Web, agrupando formas
- projetando páginas da Web, agrupando formas
- linguagem VML (VML), agrupando formas
- VML (linguagem VML), agrupando formas
- gráficos vetoriais, formas de agrupação
- Formas de VML, agrupando
- agrupando formas
- linguagem VML (VML), elemento group
- VML (linguagem VML), elemento group
- gráficos vetoriais, elemento group
- elemento de grupo
- Elementos VML, grupo
- linguagem VML (VML), espaço de coordenadas local
- VML (linguagem VML), espaço de coordenadas local
- gráficos vetoriais, espaço de coordenadas local
- espaço de coordenadas local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc9ac6da1d38bb6b30f685ebfd0f5a1d9d6026620a0e0c65366ee021668240a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056954"
---
# <a name="grouping-shapes"></a>Agrupando formas

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Como você aprendeu, você pode facilmente desenhar formas individuais usando o VML. Nesta seção, explicaremos os benefícios de agrupar formas e como agrupar formas.

Se você tivesse muitas formas que precisavam ser dimensionada, movidas ou giradas juntas, seria entediante definir os atributos individualmente para cada forma. Além disso, você aumentaria a margem para erros. Seria melhor se você pudesse agrupar as formas e, em seguida, definir os atributos para todo o grupo.

No VML, você pode usar o elemento para agrupar várias formas para `<group>` que elas possam ser transformadas como uma unidade. Por exemplo, conforme mostrado na representação VML a seguir, você pode agrupar facilmente duas formas.


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



Quando as formas são agrupadas, elas usam [o espaço de coordenadas local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) do grupo. Portanto, as formas em um grupo podem ser dimensionados e movidos juntos. Você verá mais exemplos no tópico Usar Espaço de Coordenadas Local.

Dentro de um grupo, você pode ter quantas formas ou grupos quiser. Quando um grupo está dentro de outro grupo, ele é chamado de "grupo aninhado". Não há nenhuma limitação nos níveis de aninhamento.

Por exemplo, as linhas a seguir demonstram um grupo aninhado de três níveis. Shape3 e Shape4 estão em GroupC. Shape2 e GroupC estão em GroupB. Shape1 e GroupB estão em GroupA.


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



Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .

[![voltar ao início ](images/top.gif) Voltar ao início](#top)

## <a name="summary"></a>Resumo

Você pode usar o `<group>` elemento para agrupar várias formas para que elas possam ser transformadas como uma unidade.

 

 