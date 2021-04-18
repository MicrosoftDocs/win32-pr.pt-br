---
title: Atributo Conectortype da VML
description: Atributo Conectortype da VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105785390"
---
# <a name="vml-connectortype-attribute"></a>Atributo Conectortype da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Indica o tipo de conector usado para unir formas. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:ConnectorType = " *expressão* " >

**Comentários**

Os valores são:



| Valor    | Descrição                    |
|----------|--------------------------------|
| none     | Nenhum conector.                  |
| simples | Padrão. Um conector reto. |
| angular    | Um conector em forma de ângulo.     |
| curva   | Um conector curvo.            |



 

Esse atributo também pode ser usado por um mecanismo de regras de um editor gráfico.

*Atributo de extensões de Microsoft Office*

**Exemplo**

A forma usa uma linha reta como um conector.


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 