---
title: Atributo da esquerda da VML
description: Atributo da esquerda da VML
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454292"
---
# <a name="vml-left-attribute"></a>Atributo da esquerda da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina a posição da forma em relação ao elemento à esquerda do fluxo de documentos. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* estilo = "left: *expression* " >

**Sintaxe do script**

*elemento* . Style. Left = "*expressão*"

*expressão* = de *elemento*. Style. Left

**Comentários**

O atributo **Left** é semelhante ao atributo HTML **esquerdo** padrão para estilos.

As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas. Este atributo não será gravado para formas ancoradas em linhas.

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

O valor esquerdo da forma é definido como 1 no exemplo abaixo.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo Left](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 