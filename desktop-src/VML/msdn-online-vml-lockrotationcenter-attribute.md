---
title: Atributo LockRotationCenter de VML
description: Atributo LockRotationCenter de VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759170"
---
# <a name="vml-lockrotationcenter-attribute"></a>Atributo LockRotationCenter de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se a rotação do objeto extrudada é especificada pelo atributo [RotationAngle](msdn-online-vml-rotationangle-attribute.md) . Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *Element* lockrotationcenter = " *expressão* " >

**Sintaxe do script**

*Element* . lockrotationcenter = "*expressão*"

*expressão* = de *elemento*. lockrotationcenter

**Comentários**

Se for **false**, a rotação será especificada pelo atributo [Orientation](msdn-online-vml-orientation-attribute.md) . O padrão é **True**.

Observe que:


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



é igual a:


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



*Atributo de extensões de Microsoft Office*

 

 