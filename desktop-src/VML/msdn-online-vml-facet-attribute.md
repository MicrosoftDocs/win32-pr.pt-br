---
title: Atributo de faceta de VML
description: Atributo de faceta de VML
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b1ae12ba31d286f1e029dcd433820e8c50acb05c86a92b2c06e1df50c73a0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681006"
---
# <a name="vml-facet-attribute"></a>Atributo de faceta de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define o número de facetas usadas para descrever superfícies curvas de uma extrusão. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *elemento* Facet = " *expressão* " >

**Sintaxe do script**

*Element* . faceta = "*expression*"

*expressão* = de *elemento*. Facet

**Comentários**

Define a maneira como um mecanismo de renderização aproximará a extrusão. Um número mais baixo indicará uma tolerância de renderização inferior ao mecanismo de renderização e produzirá mais facetas. Números mais altos farão com que a extrusão pareça mais facetada. O valor padrão é 30.000.

*Microsoft Office Atributo de extensões*

 

 