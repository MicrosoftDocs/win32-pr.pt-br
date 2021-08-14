---
title: Atributo TextPathOK do VML
description: Atributo TextPathOK do VML
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2c14d613df36c314dea75275a4d60fe8792d6dea644ef2595422e74a73dc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597450"
---
# <a name="vml-textpathok-attribute"></a>Atributo TextPathOK do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se um caminho de texto será exibido. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *elemento* textpathok=" *expressão* ">

**Sintaxe do script**

*elemento* . textpathok= "*expression*"

*expressão* = *elemento*. textpathok

**Comentários**

Se **False**, o caminho não poderá ter um caminho de texto. O padrão é **False**. Você deve ter esse atributo definido como **True** para exibir texto em um caminho.

*Atributo padrão VML*

**Exemplo**

A forma tem um caminho de texto. O texto "Hello VML" é exibido ao longo de uma curva em forma de sorriso.


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 