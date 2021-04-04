---
title: Atributo de caminho VML
description: Atributo de caminho VML
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823968"
---
# <a name="vml-path-attribute"></a>Atributo de caminho VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica a linha que compõe as bordas de uma forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* caminho = " *expression* " >

**Sintaxe do script**

*elemento* . Path = "*expressão*"

*expressão* = de *elemento*. Path

**Comentários**

Se uma forma contiver o elemento [path](msdn-online-vml-path-element.md) , os comandos Path do elemento Path têm precedência sobre o valor do atributo Shape. Consulte o tópico elemento **path** para obter detalhes sobre o conjunto de comandos usado para caminhos.

*Atributo padrão da VML*

**Exemplo**

Um caminho quadrado fechado é definido na cadeia de caracteres do atributo Path. Um ponto inicial é definido com `m` (usado para o comando **MoveTo** ) em 1, 1 e uma linha é desenhada com `l` (a letra "L" usada para a **linha** de comando) da posição inicial (1, 1) para os outros três pontos (em ordem): 1.200; 200.200; 200, 1. A linha é fechada com `x` (**Close**) e terminada com `e` (**end**). Observe que as coordenadas são fornecidas no espaço de coordenadas relativo e que o tamanho real é determinado pela **largura** e **altura**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo de atributo path](/previous-versions/bb264089(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 