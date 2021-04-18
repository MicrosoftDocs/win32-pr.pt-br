---
title: Atributo CoordSize de VML
description: Atributo CoordSize de VML
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105788855"
---
# <a name="vml-coordsize-attribute"></a>Atributo CoordSize de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica as unidades horizontais e verticais do retângulo que limita uma forma. Leitura/gravação. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* coordsize = " *expressão* " >

**Sintaxe do script**

*Element* . coordsize = "*expressão*"

*expressão* = de *elemento*. coordsize

**Comentários**

Se não for especificado, o tamanho da coordenada será o mesmo da caixa delimitadora da forma.

Observe que esse atributo é um vetor e que as unidades são relativas ao comprimento e à largura do retângulo delimitador.

Observe também que o mapeamento entre **coordsize** e a caixa delimitadora pode se tornar anisotropic. Verifique se a **largura de coordsize** e a **altura de coordsize** são iguais à **largura** e **altura** do estilo se você não quiser distorcer a forma.

No script, como esse é um vetor 2D, você pode acessar os valores x e y separadamente e também pode determinar o tipo de unidades esperado.

*Atributo padrão da VML*

**Exemplo**

A forma tem 100 pontos de altura alta e 100 pontos, mas cada unidade horizontal e vertical no espaço de coordenadas é 1/10 de um ponto.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo do atributo CoordSize](/previous-versions/bb229665(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 