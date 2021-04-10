---
title: Atributo de altura da VML
description: Atributo de altura da VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084643"
---
# <a name="vml-height-attribute"></a>Atributo de altura da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica a altura da forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* Style = "altura: *expressão* " >

**Sintaxe do script**

*elemento* . Style. Height = "*expressão*"

*expressão* = de *elemento*. Style. Height

**Comentários**

O atributo de **altura** é semelhante ao atributo de **altura** padrão de HTML para estilos.

As unidades podem ser mapeadas para o elemento pai ou podem estar em unidades absolutas.

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

A altura da forma é definida como 30.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



[Exemplo de atributo Height](/previous-versions/bb229671(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 