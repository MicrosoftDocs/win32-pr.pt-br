---
title: Atributo de largura da VML
description: Atributo de largura da VML
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105770586"
---
# <a name="vml-width-attribute"></a>Atributo de largura da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a largura da forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* Style = "largura: *expressão* " >

**Sintaxe do script**

*elemento* . Style. Width = "*expressão*"

*expressão* = de *elemento*. Style. Width

**Comentários**

O atributo de **largura** é semelhante ao atributo de **largura** HTML padrão para estilos.

As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas.

Os valores são:



| Valor      | Descrição                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automático       | Posição padrão de um elemento no fluxo da página.                                                                                                          |
| units      | Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex). Se nenhuma unidade for fornecida, serão assumidos pixels (px). |
| percentage | Valor expresso como uma porcentagem da largura do objeto pai.                                                                                                    |



 

*Atributo padrão da VML*

**Consulte também**

[Unidades](msdn-online-vml-units.md)

**Exemplo**

A largura da forma é 25.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



[Exemplo de atributo de largura](/previous-versions/bb264101(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 