---
title: Atributo LockRotationCenter VML
description: Atributo LockRotationCenter VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ef0cfee24998cfa343265569274ace688a05f90a270b721317394e59589a51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598054"
---
# <a name="vml-lockrotationcenter-attribute"></a>Atributo LockRotationCenter VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se a rotação do objeto extruded é especificada pelo atributo [RotationAngle.](msdn-online-vml-rotationangle-attribute.md) Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *elemento* lockrotationcenter=" *expressão* ">

**Sintaxe do script**

*element* .lockrotationcenter="*expression*"

*expressão* = *elemento*.lockrotationcenter

**Comentários**

Se **False**, a rotação será especificada pelo [atributo Orientation.](msdn-online-vml-orientation-attribute.md) O padrão é **True**.

Observe que:


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



é igual a:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Microsoft Office Atributo Extensions*

 

 