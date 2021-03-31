---
title: VML V-atributo de altura da mesma letra
description: VML V-atributo de altura da mesma letra
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641215"
---
# <a name="vml-v-same-letter-heights-attribute"></a>VML V-atributo de altura da mesma letra

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se todas as letras terão a mesma altura, independentemente do caso inicial. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *elemento* Style = "v-mesma-Letter-altura: *expression* " >

**Sintaxe do script**

*elemento* . Style. v-mesma letra-altura = "*expressão*"

*expressão* = de *elemento*. Style. v-mesma letra-altura

**Comentários**

Se **for true**, as letras minúsculas serão esticadas para a altura das letras maiúsculas. O valor padrão é **Falso**.

*Atributo padrão da VML*

**Exemplo**

Todas as letras terão a mesma altura, independentemente do caso.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 