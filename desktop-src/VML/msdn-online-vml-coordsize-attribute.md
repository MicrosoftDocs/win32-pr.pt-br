---
title: Atributo CoordSize VML
description: Atributo CoordSize VML
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9ce79507e789c38512e775100aa27eda25dc61d5f2af56f9a677daf04d238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999186"
---
# <a name="vml-coordsize-attribute"></a>Atributo CoordSize VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica as unidades horizontais e verticais do retângulo que delimita uma forma. Leitura/gravação. [IVgVector2D.](msdn-online-vml-ivgvector2d-data-type.md)

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* coordsize=" *expressão* ">

**Sintaxe do script**

*element* .coordsize="*expression*"

*expressão* = *elemento*.coordsize

**Comentários**

Se não for especificado, o tamanho da coordenada será o mesmo que a caixa delimitada da forma.

Observe que esse atributo é um vetor e que as unidades são relativas ao comprimento e à largura do retângulo delimitado.

Observe também que o mapeamento **entre coordsize** e a caixa delimitada pode se fazer aniso. Certifique-se **de** que a largura e a altura de  **coordsize coordsize** seja a mesma que a largura e a altura do estilo se você não quiser distorcer a forma. 

No script, como esse é um vetor 2D, você pode acessar os valores x e y separadamente e também pode determinar o tipo de unidades esperado.

*Atributo padrão VML*

**Exemplo**

A forma tem 100 pontos de altura e 100 pontos de largura, mas cada unidade horizontal e vertical no espaço de coordenadas é de 1/10 de um ponto.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo de atributo coordsize](/previous-versions/bb229665(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 