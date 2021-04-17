---
title: Atributo de renderização de VML
description: Atributo de renderização de VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760800"
---
# <a name="vml-render-attribute"></a>Atributo de renderização de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o modo de renderização da extrusão. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *elemento* render = " *expressão* " >

**Sintaxe do script**

*elemento* . render = "*expressão*"

*expressão* = de *elemento*. render

**Comentários**

Os valores são:



| Valor        | Descrição                                                   |
|--------------|---------------------------------------------------------------|
| consolidou        | A renderização exibe uma forma sólida. Padrão.                    |
| wireframe    | A renderização exibe uma forma de wireframe.                         |
| boundingcube | Renderização exibe o cubo delimitador que contém a forma. |



 

*Atributo de extensões de Microsoft Office*

 

 