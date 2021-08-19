---
title: Atributo de Font-Weight VML
description: Atributo de Font-Weight VML
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14dd5edb3fed869390edeff514471359162ee39fd1d78796af3d2a260c96bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754637"
---
# <a name="vml-font-weight-attribute"></a>Atributo de Font-Weight VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a espessura das letras da fonte. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Textpath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *element* style="font-weight: *expression* ">

**Sintaxe do script**

*expressão* element .style.fontweight=""

*expressão* = *elemento*.style.fontweight

**Comentários**

Os valores são os mesmos que os atributos de estilo HTML padrão. Os valores são:



| Valor   | Descrição                                                                 |
|---------|-----------------------------------------------------------------------------|
| normal  | Normal. Padrão.                                                            |
| negrito    | Negrito.                                                                       |
| bolder  | Mais pesada do que o normal.                                                        |
| lighter | Mais leve do que o normal.                                                        |
| 100     | Pelo menos tão leve quanto o peso de 200.                                        |
| 200     | Pelo menos tão negrito quanto o peso de 100 e pelo menos tão leve quanto o peso de 300. |
| 300     | Pelo menos tão negrito quanto o peso de 200 e pelo menos tão leve quanto o peso 400. |
| 400     | Normal.                                                                     |
| 500     | Pelo menos tão negrito quanto o peso 400 e pelo menos tão leve quanto o peso de 600. |
| 600     | Pelo menos tão negrito quanto o peso de 500 e pelo menos tão leve quanto o peso de 700. |
| 700     | Negrito.                                                                       |
| 800     | Pelo menos tão negrito quanto o peso de 700 e pelo menos tão leve quanto o peso de 900. |
| 900     | Pelo menos tão negrito quanto o peso 800.                                         |



 

*Atributo padrão VML*

**Exemplo**

O peso da fonte está em negrito.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 