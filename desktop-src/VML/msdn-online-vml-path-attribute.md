---
title: Atributo de caminho VML
description: Atributo de caminho VML
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f314956452db5a88011a147fd05302483e50cbce3724cf8188068770ec492db6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136959"
---
# <a name="vml-path-attribute"></a>Atributo de caminho VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica a linha que comiza as bordas de uma forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* path=" *expressão* ">

**Sintaxe do script**

*element* .path="*expression*"

*expressão* = *elemento*.path

**Comentários**

Se uma forma contiver [o elemento Path,](msdn-online-vml-path-element.md) os comandos de caminho do elemento Path têm precedência sobre o valor do atributo de forma. Consulte o **tópico Elemento Path** para obter detalhes sobre o conjunto de comandos usado para caminhos.

*Atributo padrão VML*

**Exemplo**

Um caminho quadrado fechado é definido na cadeia de caracteres do atributo path. Um ponto inicial é definido com (usado para o comando moveto) em 1,1 e uma linha é desenhada com (a letra "L" usada para o lineto de comando ) da posição inicial (1,1) para os outros três pontos `m`  `l` (em ordem): 1.200; 200.200; 200,1. A linha é fechada com `x` (**fechar**) e termina com `e` (**end**). Observe que as coordenadas são fornecidas no espaço de coordenadas relativo e que o tamanho real é determinado pela **largura** **e** altura .


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo de atributo path](/previous-versions/bb264089(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 