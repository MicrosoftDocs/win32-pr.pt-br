---
title: Atributo de visibilidade de VML
description: Atributo de visibilidade de VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105763810"
---
# <a name="vml-visibility-attribute"></a>Atributo de visibilidade de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se uma forma é exibida. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* Style = "visibilidade: *expressão* " >

**Sintaxe do script**

*elemento* . Style. Visibility = "*expressão*"

*expressão* = de *elemento*. Style. Visibility

**Comentários**

O atributo de **visibilidade** é semelhante ao atributo de **visibilidade** HTML padrão para estilos.

Os valores são:



| Valor    | Descrição                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| visible  | A forma está visível.                                                                                                                                                                   |
| oculto   | A forma não é visível, mas ainda faz parte do fluxo dos objetos no navegador. Eventos de mouse não são processados.                                                                  |
| inherit  | Padrão. O estado de visibilidade é herdado do pai da forma. Microsoft Office aplicativos usam somente **Inherit** e **Hidden**; todos os outros valores são mapeados para **herdar**. |
| recolher | Usado para aplicativos de edição gráfica que podem recolher grupos de formas; por exemplo, contornos.                                                                                     |



 

*Atributo padrão da VML*

**Exemplo**

O código a seguir cria uma forma, mas a torna oculta. Outros objetos no documento fluirão em lugar dele, deixando um espaço com o mesmo tamanho da forma.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[Exemplo de atributo Visibility](/previous-versions/bb264100(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 