---
title: Atributo do método VML
description: Atributo do método VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789620"
---
# <a name="vml-method-attribute"></a>Atributo do método VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o método usado para gerar um preenchimento gradual. Leitura/gravação. **VgSigmaType**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* Method = " *expression* " >

**Sintaxe do script**

*elemento* . Method = "*expression*"

*expressão* = de *elemento*. Method

**Comentários**

Os valores são:



| Valor  | Descrição          |
|--------|----------------------|
| Nenhum   | Nenhum preenchimento Sigma.       |
| Linear | Preenchimento Sigma linear.   |
| Sigma  | Preenchimento Sigma. Padrão. |
| Qualquer    | Qualquer preenchimento Sigma.      |



 

*Atributo padrão da VML*

**Exemplo**

A forma terá um preenchimento de gradiente linear vermelho.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 