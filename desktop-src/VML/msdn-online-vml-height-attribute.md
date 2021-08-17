---
title: Atributo de altura do VML
description: Atributo de altura do VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49218b83834d0d276d458656376d1806089be00a2158f271e38a4ee8da8099c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136989"
---
# <a name="vml-height-attribute"></a>Atributo de altura do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica a altura da forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* style="height: *expression* ">

**Sintaxe do script**

*elemento* .style.height="*expression*"

*expressão* = *elemento*.style.height

**Comentários**

O **atributo Height** é semelhante ao atributo Padrão de **Altura** html para estilos.

As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas.

Os valores são:



| Valor      | Descrição                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Posição padrão de um elemento no fluxo da página.                                                                                                          |
| units      | Um número com um designador de unidades absolutas (cm, mm, in, pt, pc ou px) ou um designador de unidades relativas (em ou ex). Se nenhuma unidade for dada, será assumido pixels (px). |
| percentage | Valor expresso como uma porcentagem da altura do objeto pai.                                                                                                   |



 

*Atributo padrão VML*

**Consulte também**

[Unidades](msdn-online-vml-units.md)

**Exemplo**

A altura da forma é definida como 30.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



[Exemplo de atributo height](/previous-versions/bb229671(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 