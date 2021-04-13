---
title: Atributo Position (forma) (VML)
description: Atributo Position (forma) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366663"
---
# <a name="position-attribute-shapevml"></a>Atributo Position (forma) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o tipo de posicionamento usado para posicionar um elemento. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* Style = "posição: *expressão* " >

**Sintaxe do script**

*elemento* . Style. Position = "*expressão*"

*expressão* = de *elemento*. Style. Position

**Comentários**

O atributo **Position** é semelhante ao atributo de **posição** HTML padrão usado com folhas de estilo.

Os valores são:



| Valor    | Descrição                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static   | Padrão. O elemento é posicionado de acordo com o fluxo normal da página. Os atributos **superior** e **esquerdo** são ignorados. Se o objeto for ancorado embutido, o que acontece apenas no Microsoft Word, esse valor será usado. |
| absoluto | O elemento é posicionado em relação ao pai, usando os atributos **superior** e **esquerdo** . Esse valor é usado por objetos flutuantes do Microsoft Word e do Microsoft Excel e slides do Microsoft PowerPoint.                  |
| relative | O elemento é posicionado de acordo com o fluxo normal da página, mas os atributos **superior** e **esquerdo** são usados. A sobreposição de elementos sobrepostos é regida pelo atributo **Z-index** .                       |



 

*Atributo padrão da VML*

**Exemplo**

A posição do retângulo é exibida usando o estilo *relativo* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo de posição](/previous-versions/bb264090(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 