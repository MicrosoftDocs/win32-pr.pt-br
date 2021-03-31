---
title: Atributo superior da VML
description: Atributo superior da VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641335"
---
# <a name="vml-top-attribute"></a>Atributo superior da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a posição da forma em relação ao elemento acima dele no fluxo da página. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* Style = "Top: *expression* " >

**Sintaxe do script**

*Element* . Style.Top = "*expressão*"

*expressão* = de *elemento*. Style.Top

**Comentários**

O atributo **Top** é semelhante ao atributo HTML **Top** padrão para estilos.

As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas. Este atributo não pode ser gravado para formas ancoradas em linhas.

Os valores são:



| Valor      | Descrição                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Automático       | Posição padrão de um elemento no fluxo da página.                                                                                                          |
| units      | Um número com um designador de unidades absolutas (cm, mm, em, pt, PC ou px) ou um designador de unidades relativas (em ou ex). Se nenhuma unidade for fornecida, serão assumidos pixels (px). |
| percentage | Valor expresso como uma porcentagem da altura do objeto pai.                                                                                                   |



 

*Atributo padrão da VML*

**Consulte também**

[Unidades](msdn-online-vml-units.md)

**Exemplo**

A borda superior da forma é de 5 pixels abaixo do objeto que a precede no fluxo da página.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo Top](/previous-versions/bb264098(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 