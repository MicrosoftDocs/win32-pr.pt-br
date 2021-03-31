---
title: Atributo de tipo (extrusão) (VML)
description: Atributo de tipo (extrusão) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823872"
---
# <a name="type-attribute-extrusionvml"></a>Atributo de tipo (extrusão) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a maneira como a forma é extrudada. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: tipo de *elemento* = " *expressão* " >

**Sintaxe do script**

*elemento* . Type = "*expressão*"

*expressão* = de *elemento*. Type

**Comentários**

Os valores são:



| Valor       | Descrição                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parallel    | A extrusão é renderizada para que o centro da projeção esteja infinitamente distante; ou seja, as linhas de extrusão não convergem (ao contrário das projeções de perspectiva). Padrão. |
| perspectiva | A extrusão é renderizada em um centro de projeção, que é o mesmo que o ponto de fuga para objetos não girados.                                                       |



 

**Atributo de extensões de Microsoft Office**

 

 