---
title: Atributo ColorMode da VML
description: Atributo ColorMode da VML
ms.assetid: 92c885ca-7912-42ff-8f07-e6e779e0ef05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7126a3f5a95910eb85007fe9a80d500c5233e5e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366230"
---
# <a name="vml-colormode-attribute"></a>Atributo ColorMode da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina o modo de cor da extrusão. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *elemento* ColorMode = " *expressão* " >

**Sintaxe do script**

*elemento* . ColorMode = "*expressão*"

*expressão* = de *elemento*. ColorMode

**Comentários**

Os valores são:



| Valor  | Descrição                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------|
| auto   | Especifica que a cor da extrusão é igual à cor de preenchimento da forma. Padrão.                |
| custom | Especifica que a extrusão será a cor do atributo [Color](color-attribute--extrusion--vml.md) . |



 

*Atributo de extensões de Microsoft Office*

 

 