---
title: Atributo Position (Shape)(VML)
description: Atributo Position (Shape)(VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ffede6653fd865c254392ffbab0bc3feac2f5e0bf51046fc85398306842dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475067"
---
# <a name="position-attribute-shapevml"></a>Atributo Position (Shape)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o tipo de posicionamento usado para colocar um elemento. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* style="position: *expression* ">

**Sintaxe do script**

*elemento* .style.position="*expression*"

*expressão* = *elemento*.style.position

**Comentários**

O **atributo Position** é semelhante ao atributo De **posição** HTML padrão usado com folhas de estilos.

Os valores são:



| Valor    | Descrição                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static   | Padrão. O elemento é posicionado de acordo com o fluxo normal da página. Os **atributos Superior** **e** Esquerdo são ignorados. Se o objeto estiver ancorado em linha, o que acontece apenas Microsoft Word, esse valor será usado. |
| absoluto | O elemento é posicionado em relação ao pai, usando os **atributos Superior** **e** Esquerdo. Esse valor é usado por Microsoft Word e Microsoft Excel objetos flutuantes e o Microsoft PowerPoint slides.                  |
| relative | O elemento é posicionado de acordo com o fluxo normal da página, mas os atributos **Superior** **e** Esquerdo são usados. A sobreposição de elementos sobrepostos é regida pelo **atributo Z-Index.**                       |



 

*Atributo padrão VML*

**Exemplo**

A posição do retângulo é exibida usando o *estilo* relativo.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo Position](/previous-versions/bb264090(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 