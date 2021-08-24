---
title: Atributo de cadeia de caracteres VML
description: Atributo de cadeia de caracteres VML
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0428c6742b145b77afe5dce27017ffcdc04d1b021cfc7ce570c9db93dd218021
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654746"
---
# <a name="vml-string-attribute"></a>Atributo de cadeia de caracteres VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define o texto do caminho do texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *Element* String = " *expressão* " >

**Sintaxe do script**

*Element* . String = "*expressão*"

*expressão* = de *elemento*. String

**Comentários**

Você deve atribuir uma cadeia de texto para exibir texto em um caminho de texto.

Atributo padrão da VML

**Exemplo**

A cadeia de caracteres que será exibida é "texto em VML".


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 