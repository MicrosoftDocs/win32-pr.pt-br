---
title: Atributo de corte de VML
description: Atributo de corte de VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05f7463465c10abb4f4f01267a7ebeac878cbf36c41f1effde6ec218bad1088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974606"
---
# <a name="vml-trim-attribute"></a>Atributo de corte de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Determina se o espaço extra é removido acima e abaixo do texto. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *Element* Style = "arrumar: *expression* " >

**Sintaxe do script**

*elemento* . Style. Trim = "*expressão*"

*expressão* = de *elemento*. Style. Trim

**Comentários**

Se **for true**, o espaço reservado para ascendentes e descendentes será removido. O valor padrão é **Falso**.

*Atributo padrão da VML*

**Exemplo**

O espaço extra acima e abaixo é cortado.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 