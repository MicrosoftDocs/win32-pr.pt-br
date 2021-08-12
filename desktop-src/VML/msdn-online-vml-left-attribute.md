---
title: Atributo esquerdo do VML
description: Atributo esquerdo do VML
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c067b15281277a85f707f6152fa855c51ee49aba439b16c009f6ff029139a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599284"
---
# <a name="vml-left-attribute"></a>Atributo esquerdo do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina a posição da forma em relação ao elemento à esquerda dela no fluxo do documento. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* style="left: *expression* ">

**Sintaxe do script**

*expressão element* .style.left=""

*expressão* = *elemento*.style.left

**Comentários**

O **atributo Left** é semelhante ao atributo PADRÃO HTML **Left** para estilos.

As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas. Esse atributo não será escrito para formas ancoradas em linha.

Os valores são:



| Valor      | Descrição                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posição padrão de um elemento no fluxo da página.                                                                                                          |
| units      | Um número com um designador de unidades absolutas (cm, mm, in, pt, pc ou px) ou um designador de unidades relativas (em ou ex). Se nenhuma unidade for dada, será assumido pixels (px). |
| percentage | Valor expresso como uma porcentagem da largura do objeto pai.                                                                                                    |



 

*Atributo padrão VML*

**Consulte também**

[Unidades](msdn-online-vml-units.md)

**Exemplo**

O valor esquerdo da forma é definido como 1 no exemplo abaixo.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo à esquerda.](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md) (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 